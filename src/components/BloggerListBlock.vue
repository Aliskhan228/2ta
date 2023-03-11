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
          <a-select class="blogger-list__sort" placeholder="По количеству просмотров"></a-select>
        </div>

        <a-list
          class="blogger-list__bloggers demo-loadmore-list"
          :loading="initLoading"
          item-layout="horizontal"
          :data-source="list"
        >
          <template #loadMore>
            <div
              v-if="!initLoading && !loading"
            >
              <a-button @click="onLoadMore">Показать еще</a-button>
            </div>
          </template>
          <template #renderItem="{ item }">
            <a-skeleton :loading="!!item.loading" active>
              <YouTubeCard :avatarSrc="item.picture.large" />
            </a-skeleton>
          </template>
        </a-list>
      </div>
      <a-list class="demo-loadmore-list" :loading="initLoading" item-layout="horizontal" :data-source="list">
        <template #renderItem="{ item }">
          <a-skeleton :loading="!!item.loading" active>
            <YouTubeCard :avatarSrc="item.picture.large" />
          </a-skeleton>
        </template>
        <template #loadMore>
          <div v-if="!initLoading && !loading"
            :style="{ textAlign: 'center', marginTop: '12px', height: '32px', lineHeight: '32px' }">
            <a-button @click="onLoadMore">Показать еще</a-button>
          </div>
        </template>
      </a-list>
    </div>
  </section>
</template>
<script>
import { defineComponent, onMounted, ref, nextTick } from 'vue';
import { DownloadOutlined } from "@ant-design/icons-vue";
import YouTubeCard from './YouTubeCard.vue';
const count = 1;
const fakeDataUrl = `https://randomuser.me/api/?results=${count}&inc=name,gender,email,nat,picture&noinfo`;
export default defineComponent({
  components: { DownloadOutlined, YouTubeCard },
  setup() {
    const initLoading = ref(true);
    const loading = ref(false);
    const data = ref([]);
    const list = ref([]);
    onMounted(() => {
      fetch(fakeDataUrl).then(res => res.json()).then(res => {
        initLoading.value = false;
        data.value = res.results;
        list.value = res.results;
      });
    });
    const onLoadMore = () => {
      loading.value = true;
      list.value = data.value.concat([...new Array(count)].map(() => ({
        loading: true,
        name: {},
        picture: {},
      })));
      fetch(fakeDataUrl).then(res => res.json()).then(res => {
        const newData = data.value.concat(res.results);
        loading.value = false;
        data.value = newData;
        list.value = newData;
        nextTick(() => {
          // Smooth scroll to bottom
          window.scrollTo({ left: 0, top: document.body.scrollHeight, behavior: "smooth" });
        });
      });
    };
    return {
      loading,
      initLoading,
      data,
      list,
      onLoadMore,
    };
  },
});
</script>
<style scoped>
.demo-loadmore-list {
  min-height: 350px;
}
</style>