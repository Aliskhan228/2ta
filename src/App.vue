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

// 1. В Filters block из под селекта тематики теперь справа вылазят нижние элементы
// 2. Поработать над всеми елементами (инпутами/селектами/тегами...), округлить их бордеры как на макете
// 3. Задать дефолтный цвет для всех тегов селекта
// 4. Для тегов добавить модифиткатор цвета
// 5. Точка возле %ЦА это <a-badge color="#f50" text="#f50" />
// 6. Ухватится за блок с подсказками и сделать его для каждой подсказки как в макете
// 7. Для кнопки соцсети youtube в стилях зачем-то прописан цвет текста, это нужно учитывать везде, т. к. из-за этого я не смогу поменять type кнопки чтобы все просто работало, придется лезть в стили и разбиратся с ними
// 8. Цвет слайдера

</script>