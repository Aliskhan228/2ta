<template>
  <a-card class="blogger-list__card blogger-list__card_youtube">
    <div class="blogger-list__card-top">
      <a-avatar class="blogger-list__card-avatar" :src="avatarSrc" />
      <div>
        <div class="blogger-list__card-name">
          <div>
            <h2>FOSTI</h2>
            <a-tooltip class="blogger-list__tooltip tooltip" placement="top">
              <template #title>
                <span class="tooltip-text"> Убрать из выгрузки </span>
              </template>
              <MinusCircleTwoTone class="remove-icon" />
            </a-tooltip>
          </div>
        </div>
        <div class="blogger-list__card-tags filters-tags__list">
          <a-tag class="filter-tag filter-tag_green">Аниме и комиксы</a-tag>
          <a-tag class="filter-tag">Анимация</a-tag>
          <a-tag class="filter-tag">Игры</a-tag>
          <a-tag class="filter-tag">Мультфильмы</a-tag>
        </div>
      </div>

      <div class="blogger-list__card-description blogger-list__card_youtube">
        <div class="blogger-list__card-description-text">
          Привет гости, на связи FOSTI. Канал "FOSTI" посвещён урокам или же
          туториалам для начинающих ютуберов, по типу как сделать оформление
          канала, как сделать превью, как поднять подписчиков и многое другое.
          Здесь ты научишься азам Photoshop'a, Cinema 4d и многим другим.
          Подпишись и лето увеличивается на 1 месяц!
        </div>
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
          <RightOutlined />
        </a-popover>
      </div>
    </div>

    <div class="blogger-list__card-data blogger-list__card_youtube">
      <div class="blogger-list__card-data-items">
        <div class="blogger-list__card-data-item _er">
          <h4>ER</h4>
          <span class="bold-text">99%</span>
          <div class="er-info">
            <p>
              %ЦА
              <a-badge color="#F7B801" text="31.7%" />
              <a-tooltip
                class="blogger-list__tooltip tooltip"
                placement="right"
              >
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
            <p>
              18-35 лет
              <span class="bold-text">52.7%</span>
            </p>
            <p>
              Женщины
              <span class="bold-text">75.3%</span>
            </p>
          </div>
        </div>
        <div class="blogger-list__card-data-item _subs">
          <h4>Подписчики</h4>
          <span class="bold-text">555 000</span>
        </div>
        <div class="blogger-list__card-data-item _views">
          <h4>Просмотры</h4>
          <span class="bold-text">248 256 370</span>
          <div class="views-info">
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
        </div>
        <div class="blogger-list__card-data-item _price">
          <h4>Цена за обзор</h4>
          <span class="bold-text">555 000 ₽</span>
          <a-tooltip class="blogger-list__tooltip tooltip" placement="right">
            <template #title>
              <span>
                Цена предсказана алгоритмами на основе исторических значений
              </span>
            </template>
            <InfoCircleOutlined class="tooltip-icon" />
          </a-tooltip>
        </div>
      </div>

      <div class="blogger-list__card-buttons">
        <a-button
          class="blogger-list__card-btn blogger-list__card-btn_contact"
          type="primary"
        >
          <div>
            <IconMessage />
            Связаться
          </div>
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
  InfoCircleOutlined,
} from "@ant-design/icons-vue";
import IconMessage from "./icons/IconMessage.vue";
export default {
  components: {
    MinusCircleTwoTone,
    MessageOutlined,
    RightOutlined,
    QuestionCircleOutlined,
    InfoCircleOutlined,
    IconMessage,
  },
  props: {
    avatarSrc: String,
  },
};
</script>
