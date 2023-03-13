<template>
  <a-card class="blogger-list__card blogger-list__card_instagram">
    <div class="blogger-list__card-top">
      <a-avatar class="blogger-list__card-avatar" :src="avatarSrc" />
      <div>
        <div class="blogger-list__card-name">
          <h2>anushkasharma</h2>
          <CheckCircleFilled class="verified-icon" />
          <a-tooltip class="blogger-list__tooltip tooltip" placement="top">
            <template #title>
              <span class="tooltip-text"> Убрать из выгрузки </span>
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


      <div class="blogger-list__card-description">
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
              канала, как сделать превью, как поднять подписчиков и многое другое.
              Здесь ты научишься азам Photoshop'a, Cinema 4d и многим другим.
              Подпишись и лето увеличивается на 1 месяц!
            </div>
          </template>
          <RightOutlined />
        </a-popover>
      </div>
    </div>

    <div class="blogger-list__card-data">
      <div class="blogger-list__card-data-items">
        <div class="blogger-list__card-data-item _review">
          <h4>Обзор</h4>
          <div class="review-info">
            <p class="first-child">
              ER
              <span>7.87%</span>
            </p>
            <p>
              Подписчики
              <span>62 324 739</span>
            </p>
            <p>
              Подписки
              <span>547</span>
            </p>
            <p>
              Посл. публикация
              <span>2023-01-02</span>
            </p>
          </div>
          <div class="blogger-list__card-data-item-buttons">
            <a-button>Скачать подписчиков</a-button>
            <a-button>Скачать подписки</a-button>
          </div>
        </div>
        <div class="blogger-list__card-data-item _prices">
          <h4>Цены</h4>
          <div class="prices-info">
            <p>
              Пост
              <span class="bold-text">255 000 ₽</span>
              <a-tooltip class="blogger-list__tooltip tooltip" placement="right">
                <template #title>
                  <span> Цена </span>
                </template>
                <InfoCircleOutlined class="tooltip-icon" />
              </a-tooltip>
            </p>
            <p>
              3 поста
              <span class="bold-text">600 000 ₽</span>
              <a-tooltip class="blogger-list__tooltip tooltip" placement="right">
                <template #title>
                  <span> Цена </span>
                </template>
                <InfoCircleOutlined class="tooltip-icon" />
              </a-tooltip>
            </p>
            <p>
              Видео
              <span class="bold-text">520 000 ₽</span>
            </p>
            <p>
              Reels
              <span class="bold-text">680 000 ₽</span>
            </p>
          </div>
        </div>
        <div class="blogger-list__card-data-item _ta">
          <h4>ЦА</h4>
          <div class="ta-info">
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
        <div class="blogger-list__card-data-item _reels">
          <h4>Reels</h4>
          <div class="reels-info">
            <p class="first-child">
              <EyeOutlined />
              в среднем
              <span>14 217 118</span>
            </p>
            <p>
              <LikeOutlined />
              в среднем
              <span>732 123</span>
            </p>
            <p>
              <MessageOutlined />
              в среднем
              <span>2 105</span>
            </p>
            <p>
              ER
              <span>7.01%</span>
            </p>
            <p>
              Кол-во
              <span>14</span>
            </p>
            <p>
              Посл.
              <span>2023-02-08</span>
            </p>
          </div>
        </div>
        <div class="blogger-list__card-data-item _video">
          <h4>Видео</h4>
          <div class="video-info">
            <p class="first-child">
              <EyeOutlined />
              в среднем
              <span>14 217 118</span>
            </p>
            <p>
              <LikeOutlined />
              в среднем
              <span>732 123</span>
            </p>
            <p>
              <MessageOutlined />
              в среднем
              <span>2 105</span>
            </p>
            <p>
              ER
              <span>5.63%</span>
            </p>
            <p>
              Кол-во
              <span>11</span>
            </p>
            <p>
              Посл.
              <span>2023-02-08</span>
            </p>
          </div>
        </div>
        <div class="blogger-list__card-data-item _photo">
          <h4>Фото</h4>
          <div class="photo-info">
            <p class="first-child">
              <LikeOutlined />
              в среднем
              <span>732 123</span>
            </p>
            <p>
              <MessageOutlined />
              в среднем
              <span>2 105</span>
            </p>
            <p>
              ER
              <span>4.73%</span>
            </p>
            <p>
              Кол-во
              <span>19</span>
            </p>
            <p>
              Посл.
              <span>2023-02-08</span>
            </p>
          </div>
        </div>
      </div>

      <div class="blogger-list__card-buttons">
        <a-button class="blogger-list__card-btn blogger-list__card-btn_contact" type="primary">
          <div style="display: flex; align-items: center; gap: 7px;">
            <IconMessage />
            Связаться
          </div>
        </a-button>
        <a-button class="blogger-list__card-btn blogger-list__card-btn_analise">Полный анализ</a-button>
        <a-button class="blogger-list__card-btn blogger-list__card-btn_analise">Похожие аккаунты</a-button>
        <a-button class="blogger-list__card-btn blogger-list__card-btn_contacts">Контакты</a-button>
      </div>
    </div>

    <div class="blogger-list__card-bottom">
      <div class="blogger-list__card-bottom-item">
        <h4>Бренды</h4>
        <div class="blogger-list__card-data-item-buttons">
          <a-button>Myntra</a-button>
          <a-button>Slurrpfarm</a-button>
          <a-button>@Ankitmalik3</a-button>
          <a-button>@Toothsi_Aligner</a-button>
          <a-button>Blue</a-button>
          <a-button>World</a-button>
          <a-button>Centrum Women</a-button>
          <a-button>Hyaluronate</a-button>
        </div>
      </div>
      <div class="blogger-list__card-bottom-item">
        <h4>География постов</h4>
        <div class="blogger-list__card-data-item-buttons">
          <a-button>Emirates Stadium</a-button>
          <a-button>London, UK</a-button>
          <a-button>Arsenal Training Centre</a-button>
          <a-button>Hale End Academy</a-button>
          <a-button>Europe</a-button>
        </div>
      </div>
      <div class="blogger-list__card-bottom-item">
        <h4>Хэштеги</h4>
        <div class="blogger-list__card-data-item-buttons">
          <a-button>ad</a-button>
          <a-button>MichaelKors</a-button>
          <a-button>YesMoms</a-button>
          <a-button>Millet</a-button>
          <a-button>BlueTribeFoods</a-button>
          <a-button>PlantFriendlyTribe</a-button>
          <a-button>ForeverFaster</a-button>
        </div>
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
  CheckCircleFilled,
  InfoCircleOutlined,
  EyeOutlined,
  LikeOutlined,
} from "@ant-design/icons-vue";
import IconMessage from "./icons/IconMessage.vue";
export default {
  components: {
    MinusCircleTwoTone,
    MessageOutlined,
    RightOutlined,
    QuestionCircleOutlined,
    CheckCircleFilled,
    InfoCircleOutlined,
    EyeOutlined,
    LikeOutlined,
    IconMessage
  },
  props: {
    avatarSrc: String,
  },
};
</script>
