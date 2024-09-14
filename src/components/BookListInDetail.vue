<template lang="pug">
  .book-list
    BookListItemInDetail(
      v-for="item in items"
      :item="item"
      :key="item.id"
      class="book-list__item"
    )
</template>

<script setup>
  import { Carousel, Slide } from 'vue3-carousel';
  import 'vue3-carousel/dist/carousel.css';
  import BookListItemInDetail from './BookListItemInDetail.vue';

  const { items } = defineProps({
    items: {
      type: Array,
      required: true
    }
  })
</script>

<style lang="scss" scoped>
  .book-list {
    display: flex;
    flex-wrap: wrap;
    align-items: flex-start;
    gap: 12px;
    padding: 6px;
    margin-top: 6px;

    &__item {
      width: 100%;
      margin-bottom: 12px;
    }

    @media (min-width: 768px) {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
    }

    @media (min-width: 1024px) {
      display: grid;
      grid-template-columns: repeat(1, 1fr);
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