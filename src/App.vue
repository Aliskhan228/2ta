<template>
  <section class="app">
    <HeaderBlock />
    <FiltersBlock />
    <FiltersTagsBlock />
    <BloggerListBlock />
  </section>
</template>
<script>
import HeaderBlock from './components/HeaderBlock.vue';
import FiltersBlock from './components/FiltersBlock.vue';
import FiltersTagsBlock from "./components/FiltersTagsBlock.vue";
import BloggerListBlock from './components/BloggerListBlock.vue';

export default {
  components: { HeaderBlock, FiltersBlock, FiltersTagsBlock, BloggerListBlock }
}
</script>