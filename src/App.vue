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
// 2. Ухватится за блок с подсказками и сделать его для каждой подсказки как в макете
// 3. Не все иконки в макете используются из фреймворка, достал иконку Message, добавил ее в карточку. В будущем все отличающиеся иконки (только svg иконки) добавляйте также
// 4. Все стили которые я набрасываю в компонентах, поправляйте и выносите в модули
// 5. Цвет кнопки Связаться - #2382F7. Поправьте, будьте внимательнее
// 6. Обратите внимание, в макете иконка выгрузки возле юзернейма больше других
// 7. Не соблюдены отступы между значениями карточек, например: Ср. просмотров 345 838, нету отступа 4px
// 8. Если решили использовать один файл стилей для карточек, переиминуйте его в card
// 9. Сейчас у карточек есть border, на макете нету
// 10. Поработайте над popover для description, он явно не такой как на макете. Также cursor pointer должен быть только на стрелке

</script>