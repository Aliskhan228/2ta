<template>
  <section class="app">
    <HeaderBlock />
    <FiltersBlock />
    <BloggerListBlock />
  </section>
</template>
<script>
import HeaderBlock from './components/HeaderBlock.vue';
import FiltersBlock from './components/FiltersBlock.vue';
import BloggerListBlock from './components/BloggerListBlock.vue';
export default {
  components: { HeaderBlock, FiltersBlock, BloggerListBlock }
}
</script>