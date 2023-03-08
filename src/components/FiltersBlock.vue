<template>
  <!-- Write HTML here -->
  <section>
    <div class="filters-block">
      <div class="container">
        <div class="filters-block__wrapper">
          <div class="filters-block__buttons">
            <a-button class="filters-block__btn youtube-btn" type="primary"
              >Youtube</a-button
            >
            <a-button class="filters-block__btn instagram-btn"
              >Instagram</a-button
            >
          </div>

          <div class="filters-block__filters-wrapper">
            <div class="filters-block__settings">
              <p class="filters-block__title filters-block__title_settings">
                Настройки ЦА
                <a-tooltip class="filters-block__tooltip" placement="right">
                  <template #title>
                    <span>
                      Не фильтрует блогеров. Выбор значений влияет на %<span
                        class="bold-text"
                        >ЦА</span
                      >
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
                <WomanOutlined
                  class="filters-block__gender-icon filters-block__gender-icon_female"
                />
                <ManOutlined
                  class="filters-block__gender-icon filters-block__gender-icon_male"
                />
              </div>

              <div class="filters-block__slider filters-block__slider_age">
                <p class="filters-block__slider-name">Возраст</p>
                <a-slider class="filters-block__slider-component"></a-slider>
              </div>

              <a-auto-complete
                class="filters-block__choose-country inputs"
                placeholder="Выберите страну"
              />
            </div>

            <div class="filters-block__filter">
              <div class="filters-block__filter-left">
                <p class="filters-block__title filters-block__title_filter">
                  Фильтры
                </p>

                <div class="filters-block__slider filters-block__slider_subs">
                  <p class="filters-block__slider-name">Подписчики</p>
                  <a-slider class="filters-block__slider-component"></a-slider>
                </div>

                <div class="filters-block__slider filters-block__slider_views">
                  <p class="filters-block__slider-name">Просмотры</p>
                  <a-slider class="filters-block__slider-component"></a-slider>
                </div>

                <div class="filters-block__date">
                  <p class="filters-block__date-name">Дата последнего видео</p>
                  <a-space class="filters-block__date-component inputs">
                    <a-range-picker />
                  </a-space>
                </div>
              </div>

              <div class="filters-block__filter-right">
                <a-select
                  class="filters-block__themes inputs"
                  placeholder="Выберите тематику"
                ></a-select>

                <a-auto-complete
                  class="filters-block__city inputs"
                  placeholder="Город блогера"
                />

                <a-checkbox class="filters-block__checkbox"
                  >Только с контактами</a-checkbox
                >
              </div>
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

export default {
  components: {
    QuestionCircleOutlined,
    ManOutlined,
    WomanOutlined,
  },
};
</script>
