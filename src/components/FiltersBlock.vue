<template>
  <!-- Write HTML here -->
  <section class="filters-block">
    <div class="container">
      <div class="filters-block__wrapper">
        <div class="filters-block__buttons">
          <a-button class="filters-block__btn youtube-btn" type="primary">Youtube</a-button>
          <a-button class="filters-block__btn instagram-btn">Instagram</a-button>
        </div>

        <div class="filters-block__filters-wrapper">
          <div class="filters-block__settings">
            <p class="filters-block__title filters-block__title_settings">
              Настройки ЦА
              <a-tooltip class="filters-block__tooltip" placement="right">
                <template #title>
                  <span>
                    Не фильтрует блогеров. Выбор значений влияет на %<span class="bold-text">ЦА</span>
                    (процент целевой аудитории) Вычисляется как %
                    <span class="bold-text">из страны аудитории</span> * %
                    <span class="bold-text">по полу</span> * %
                    <span class="bold-text">по возрасту</span>. По этому
                    значению блогеров можно сортировать.
                  </span>
                </template>
                <QuestionCircleOutlined class="filters-block__tooltip-icon" />
              </a-tooltip>
            </p>

            <div class="filters-block__gender">
              <WomanOutlined class="filters-block__gender-icon filters-block__gender-icon_female" />
              <ManOutlined class="filters-block__gender-icon filters-block__gender-icon_male" />
            </div>

            <div class="filters-block__slider filters-block__slider_age">
              <p class="filters-block__slider-name">Возраст</p>
              <a-slider class="filters-block__slider-component" v-model:value="slidersState.age.values"
                :marks="slidersState.age.marks" range :step="null" :tooltipVisible="false"
                @change="slidersState.age.handleSlider">
                <template #mark="{ label, point }">
                  <template v-if="slidersState.age.values.includes(point)">
                    <strong>{{ label }}</strong>
                  </template>
                  <template v-else>{{ label }}</template>
                </template>
              </a-slider>
            </div>
            <a-auto-complete class="filters-block__choose-country inputs" placeholder="Выберите страну" />
          </div>

          <div class="filters-block__filter">
            <div class="filters-block__filter-left">
              <p class="filters-block__title filters-block__title_filter">
                Фильтры
              </p>

              <div class="filters-block__slider filters-block__slider_subs">
                <p class="filters-block__slider-name">Подписчики</p>
                <a-slider class="filters-block__slider-component" v-model:value="slidersState.subscribers.values"
                  :marks="slidersState.subscribers.marks" range :step="null" :tooltipVisible="false"
                  @change="slidersState.subscribers.handleSlider">
                  <template #mark="{ label, point }">
                    <template v-if="slidersState.subscribers.values.includes(point)">
                      <strong>{{ label }}</strong>
                    </template>
                    <template v-else>{{ label }}</template>
                  </template>
                </a-slider>
              </div>

              <div class="filters-block__slider filters-block__slider_views">
                <p class="filters-block__slider-name">Просмотры</p>
                <a-slider class="filters-block__slider-component" v-model:value="slidersState.views.values"
                  :marks="slidersState.views.marks" range :step="null" :tooltipVisible="false"
                  @change="slidersState.views.handleSlider">
                  <template #mark="{ label, point }">
                    <template v-if="slidersState.views.values.includes(point)">
                      <strong>{{ label }}</strong>
                    </template>
                    <template v-else>{{ label }}</template>
                  </template>
                </a-slider>
              </div>

              <div class="filters-block__date">
                <p class="filters-block__date-name">Дата последнего видео</p>
                <a-space class="filters-block__date-component inputs">
                  <a-range-picker />
                </a-space>
              </div>
            </div>

            <div class="filters-block__filter-right">
              <a-select class="filters-block__themes inputs" placeholder="Выберите тематику"></a-select>

              <a-auto-complete class="filters-block__city inputs" placeholder="Город блогера" />

              <a-checkbox class="filters-block__checkbox">Только с контактами</a-checkbox>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
import {
  QuestionCircleOutlined,
  ManOutlined,
  WomanOutlined,
} from "@ant-design/icons-vue";
import { defineComponent, reactive } from 'vue';
export default defineComponent({
  components: {
    QuestionCircleOutlined,
    ManOutlined,
    WomanOutlined,
  },
  setup() {
    const slidersState = reactive({
      age: {
        values: [0, 100],
        marks: { 0: '13', 17: '18', 33: '25', 50: '35', 66: '45', 83: '65', 100: '65+' },
        handleSlider: (event) => {
          // console.log(`${slidersState.age.marks[event[0]]} - ${slidersState.age.marks[event[1]]}`)
        }
      },
      subscribers: {
        values: [0, 100],
        marks: { 0: '1k', 14: '20k', 29: '50k', 42: '100k', 56: '300k', 71: '500K', 85: '1M', 100: '1M+' },
        handleSlider: (event) => {
          // console.log(`${slidersState.subscribers.marks[event[0]]} - ${slidersState.subscribers.marks[event[1]]}`)
        }
      },
      views: {
        values: [0, 100],
        marks: { 0: '1k', 14: '20k', 29: '50k', 42: '100k', 56: '300k', 71: '500K', 85: '1M', 100: '1M+' },
        handleSlider: (event) => {
          // console.log(`${slidersState.views.marks[event[0]]} - ${slidersState.views.marks[event[1]]}`)
        }
      },
    })
    return {
      slidersState
    };
  },
});
</script>
<style lang="scss">
/* Tooltip width */
.ant-tooltip-inner { 
  min-width: 500px !important;
}

/* Disable actions by slider mark */
.ant-slider-mark {
  pointer-events: none !important;
}
</style>
