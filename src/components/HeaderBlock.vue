<template>
  <header class="header">
    <div class="container">
      <div class="header__wrapper">
        <a class="header__logo" href="#">
          <img class="logo" src="../assets/images/logo.png" alt="" />
          <h1 class="header__title">2TA</h1>
        </a>
        <h2 class="header__subtitle">
          Поиск блогеров <br />
          для рекламы
        </h2>
        <a-input-search class="header__input" placeholder="Введите запрос" />
        <a-dropdown-button class="header__dropdown">
          prepsu.satyam
          <template #icon>
            <UserOutlined />
          </template>
        </a-dropdown-button>
      </div>
    </div>
  </header>
</template>
<script>
import { UserOutlined } from "@ant-design/icons-vue";
export default {
  components: { UserOutlined },
};
</script>
