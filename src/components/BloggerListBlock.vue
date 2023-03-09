<template>
  <!-- Write HTML here -->
  <section class="blogger-list">
    <div class="container">
      <div class="blogger-list__wrapper">
        <div class="blogger-list__topbar">
          <p class="blogger-list__found">
            Найдено:
            <span class="blogger-list__found-number">119</span>
          </p>
          <a-button class="blogger-list__upload-button">
            <template #icon>
              <DownloadOutlined />
            </template>
            Выгрузить 20 результатов
          </a-button>
          <a-select class="blogger-list__sort"></a-select>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
// import FiltersTagsBlock from "./FiltersTagsBlock.vue";
import { DownloadOutlined } from "@ant-design/icons-vue";
export default {
  components: { DownloadOutlined },
};
</script>
