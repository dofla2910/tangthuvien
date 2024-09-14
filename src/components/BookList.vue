<template lang="pug">
  .book-list
    BookListItem(
      v-for="item in items"
      :item="item"
      :key="item.id"
      class="book-list__item"
    )
</template>

<script setup>
  import { Carousel, Slide } from 'vue3-carousel';
  import 'vue3-carousel/dist/carousel.css';
  import BookListItem from './BookListItem.vue';

  const { items } = defineProps({
    items: {
      type: Array,
      required: true
    }
  })

  console.log(items)
</script>

<style lang="scss" scoped>
  .book-list {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 12px;
    padding: 6px;
    margin-top: 6px;
    overflow-x: auto;

    &__item {
      width: 100%;
    }

    @media (min-width: 1200px) {
      display: flex;
      gap: 0;

      &__item {
        width: 25%;
      }
    }
  }
</style>