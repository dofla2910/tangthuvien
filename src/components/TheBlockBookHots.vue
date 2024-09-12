<template lang="pug">
  .block-hots
    .block-hots__header
      h3.block-hots__title Truyện đã hoàn thành
      a.block-hots__more(href='#')
        span Xem thêm
        FontAwesomeIcon(:icon='faAngleRight')
    .block-hots_list
      BookList
</template>

<script setup>
  import { faAngleRight } from '@fortawesome/free-solid-svg-icons';
  import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';
  import BookList from './BookList.vue';
</script>

<style lang="scss" scoped>

  .block-hots {

    &,
    &__list {
      width: 100%;
      padding: 6px;
      background-color: #fff;
    }

    &__header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      color: #33373d;
      height: 2.75rem;
      border-top: 0;
      border-bottom: .7px solid rgba(0, 0, 0, .1);
      width: 100%;
      text-transform: uppercase;
      line-height: 1.75rem;
      overflow: hidden;
      margin-bottom: 1rem;
    }

    &__title {
      font-weight: 400;
      display: inline;
      font-size: 16px;
    }

    &__title::before {
      content: '';
      display: inline-block;
      width: .6rem;
      height: 1.5em;
      vertical-align: middle;
      color: transparent;
      border-left: 2px solid #ed424b;
    }

    &__more * {
      font-size: 14px;
      font-weight: 700;
    }

    &__more:hover {
      color: #ed424b;
    }

    /*Ipad dọc(768 x 1024)*/
    @media (min-width: 768px) {
      &__header {
        height: 3.5rem;
      }

      &__title {
        font-size: 24px;
      }

      &__more * {
        font-size: 20px;
      }
    }

    /*Ipad ngang(1024 x 768)*/
    @media (min-width: 1024px) {
      &__header {
        height: 5rem;
      }

      &__title {
        font-size: 32px;
      }

      &__more * {
        font-size: 28px;
      }
    }

    @media (min-width: 1200px) {
      &__header {
        height: 2.75rem;
      }

      &__title {
        font-size: 16px;
      }

      &__more * {
        font-size: 14px;
      }
    }
  }
</style>