<template>
  <section class="app">
    <HeaderBlock />
		<FiltersBlock />
  </section>
</template>
<script>
import HeaderBlock from './components/HeaderBlock.vue';
import FiltersBlock from './components/FiltersBlock.vue';
export default {
  components: { HeaderBlock, FiltersBlock }
}
</script>