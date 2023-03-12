<template>
  <!-- <a-card class="youtube-card">
        <a-card-meta>
            <template #avatar>
                <a-avatar :src="avatarSrc" />
            </template>
            <template #title>
                <div style="display: flex; align-items: baseline; gap: 5px;">
                    <h2>Креативный канал Томо</h2>
                    <InfoCircleTwoTone />
                </div>
                <a-tag color="green">Аниме и комиксы</a-tag>
                <a-tag color="blue">Искусство и фото</a-tag>
            </template>
            <template #description>
                <a-popover placement="left">
                    <template #title>
                        <div><b>О блогере</b></div>
                    </template>
                    <template #content>
                        <div style="max-width: 300px;">Привет гости, на связи FOSTI. Канал "FOSTI" посвещён урокам или же
                            туториалам для начинающих ютуберов, по типу как сделать оформление канала, как сделать превью,
                            как поднять подписчиков и многое другое. Здесь ты научишься азам Photoshop'a, Cinema 4d и многим
                            другим. Подпишись и лето увеличивается на 1 месяц!</div>
                    </template>
                    <div class="youtube-card-description">
                        <div class="text">Привет гости, на связи FOSTI. Канал "FOSTI" посвещён урокам или же
                            туториалам для начинающих ютуберов, по типу как сделать оформление канала, как сделать превью,
                            как
                            поднять подписчиков и многое другое. Здесь ты научишься азам Photoshop'a, Cinema 4d и многим
                            другим.
                            Подпишись и лето увеличивается на 1 месяц!</div>
                    </div>
                </a-popover>

            </template>
        </a-card-meta>
        <a-avatar :src="avatarSrc" />
        <div class="youtube-card-data">
            <div>ER <a-badge color="#f50" text="#f50" /></div>
            <div>Подписчики</div>
            <div>Просмотры</div>
            <div>Цена за обзор</div>
            <div style="display: flex; flex-direction: column; gap: 5px;">
                <a-button type="primary">Связаться</a-button>
                <a-button>Полный анализ</a-button>
                <a-button>Контакты</a-button>
            </div>
				</div>
		</a-card> -->

  <a-card class="blogger-list__card blogger-list__card_youtube-card">
    <!-- <a-card-meta class="blogger-list__card-top">
      <template #avatar>
        <a-avatar class="blogger-list__card-avatar" :src="avatarSrc" />
      </template>
      <template #title>
        <div class="blogger-list__card-name">
          <h2>FOSTI</h2>
          <MinusCircleTwoTone class="remove-icon" />
        </div>
        <div class="blogger-list__card-tags filters-tags__list">
          <a-tag class="filter-tag">Анимация</a-tag>
          <a-tag class="filter-tag">Игры</a-tag>
          <a-tag class="filter-tag">Мультфильмы</a-tag>
        </div>
      </template>
      <template #description>
        <a-popover class="blogger-list__card-popover" placement="left">
          <template #title>
            <div class="blogger-list__card-popover-title"><b>О блогере</b></div>
          </template>
          <template #content>
            <div class="blogger-list__card-popover-text">
              Привет гости, на связи FOSTI. Канал "FOSTI" посвещён урокам или же
              туториалам для начинающих ютуберов, по типу как сделать оформление
              канала, как сделать превью, как поднять подписчиков и многое
              другое. Здесь ты научишься азам Photoshop'a, Cinema 4d и многим
              другим. Подпишись и лето увеличивается на 1 месяц!
            </div>
          </template>
          <div
            class="blogger-list__card-description blogger-list__card_youtube"
          >
            <div class="blogger-list__card-description-text">
              Привет гости, на связи FOSTI. Канал "FOSTI" посвещён урокам или же
              туториалам для начинающих ютуберов, по типу как сделать оформление
              канала, как сделать превью, как поднять подписчиков и многое
              другое. Здесь ты научишься азам Photoshop'a, Cinema 4d и многим
              другим. Подпишись и лето увеличивается на 1 месяц!
            </div>
						<RightOutlined />
          </div>
        </a-popover>
      </template>
    </a-card-meta> -->

    <div class="blogger-list__card-top">
      <a-avatar class="blogger-list__card-avatar" :src="avatarSrc" />
      <div>
        <div class="blogger-list__card-name">
          <h2>FOSTI</h2>
          <a-tooltip class="blogger-list__tooltip tooltip" placement="top">
            <template #title>
              <span class="tooltip-text">
                Убрать из выгрузки
              </span>
            </template>
            <MinusCircleTwoTone class="remove-icon" />
          </a-tooltip>
        </div>
        <div class="blogger-list__card-tags filters-tags__list">
          <a-tag class="filter-tag filter-tag_green">Аниме и комиксы</a-tag>
          <a-tag class="filter-tag">Анимация</a-tag>
          <a-tag class="filter-tag">Игры</a-tag>
          <a-tag class="filter-tag">Мультфильмы</a-tag>
        </div>
      </div>

      <a-popover class="blogger-list__card-popover" placement="left">
        <template #title>
          <div class="blogger-list__card-popover-title"><b>О блогере</b></div>
        </template>
        <template #content>
          <div class="blogger-list__card-popover-text">
            Привет гости, на связи FOSTI. Канал "FOSTI" посвещён урокам или же
            туториалам для начинающих ютуберов, по типу как сделать оформление
            канала, как сделать превью, как поднять подписчиков и многое другое.
            Здесь ты научишься азам Photoshop'a, Cinema 4d и многим другим.
            Подпишись и лето увеличивается на 1 месяц!
          </div>
        </template>
        <div class="blogger-list__card-description blogger-list__card_youtube">
          <div class="blogger-list__card-description-text">
            Привет гости, на связи FOSTI. Канал "FOSTI" посвещён урокам или же
            туториалам для начинающих ютуберов, по типу как сделать оформление
            канала, как сделать превью, как поднять подписчиков и многое другое.
            Здесь ты научишься азам Photoshop'a, Cinema 4d и многим другим.
            Подпишись и лето увеличивается на 1 месяц!
          </div>
          <RightOutlined />
        </div>
      </a-popover>
    </div>

    <div class="blogger-list__card-data blogger-list__card_youtube">
      <div class="blogger-list__card-data-items">
        <div class="blogger-list__card-data-item _er">
          <h4>ER</h4>
          <span class="bold-text">99%</span>
          <p>
            %ЦА
            <a-badge color="#F7B801" text="31.7%" />
            <a-tooltip class="blogger-list__tooltip tooltip" placement="right">
              <template #title>
                <span>
                  Вычисляется как %
                  <span class="bold-text">из страны аудитории *</span> %
                  <span class="bold-text">по полу *</span> %
                  <span class="bold-text">по возрасту</span>
                </span>
              </template>
              <QuestionCircleOutlined class="tooltip-icon" />
            </a-tooltip>
          </p>
        </div>
        <div class="blogger-list__card-data-item _subs">
          <h4>Подписчики</h4>
          <span class="bold-text">555 000</span>
        </div>
        <div class="blogger-list__card-data-item _views">
          <h4>Просмотры</h4>
          <span class="bold-text">248 256 370</span>
          <p class="first-child">
            Ср. просмотров
            <span>345 838</span>
          </p>
          <p>
            Кол-во видео
            <span>861</span>
          </p>
          <p>
            Посл. публикация
            <span>2023-01-02</span>
          </p>
        </div>
        <div class="blogger-list__card-data-item _price">
          <h4>Цена за обзор</h4>
          <span class="bold-text">555 000 ₽</span>
        </div>
      </div>

      <div class="blogger-list__card-buttons">
        <a-button
          class="blogger-list__card-btn blogger-list__card-btn_contact"
          type="primary"
        >
          <MessageOutlined />
          Связаться
        </a-button>
        <a-button class="blogger-list__card-btn blogger-list__card-btn_analise"
          >Полный анализ</a-button
        >
        <a-button class="blogger-list__card-btn blogger-list__card-btn_contacts"
          >Контакты</a-button
        >
      </div>
    </div>
  </a-card>
</template>
<script>
import {
  MinusCircleTwoTone,
  MessageOutlined,
  RightOutlined,
  QuestionCircleOutlined,
} from "@ant-design/icons-vue";
export default {
  components: {
    MinusCircleTwoTone,
    MessageOutlined,
    RightOutlined,
    QuestionCircleOutlined,
  },
  props: {
    avatarSrc: String,
  },
};
</script>
