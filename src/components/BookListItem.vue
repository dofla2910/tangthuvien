<template lang="pug">
  .item
    a.item__image(:href='props.item.src')
      img(:src='props.item.image', alt='')
    .item__content
      .item__title {{ props.item.title }}
</template>

<script setup>
  const props = defineProps({
    item: {
      type: Object,
      required: true
    }
  })
</script>

<style lang="scss" scoped>
  .item {
    width: 100%;
    height: 100%;

    &__image img {
      width: 100%;
      object-fit: cover;
    }

    &__title {
      text-align: center;
      font-size: 14px;
      color: #33373d;

    }

    /*Ipad dọc(768 x 1024)*/
    @media (min-width: 768px) {

      &__image img {
        padding: 0 20px;
      }

      &__title {
        font-size: 20px;
      }
    }

    /*Ipad ngang và Desktop*/
    @media (min-width: 1024px) {

      &__title {
        font-size: 24px;
      }
    }

    /*Desktop*/
    @media (min-width: 1200px) {

      &__title {
        font-size: 14px;
      }

      .carousel__slide {
        width: 20%;
      }
    }
  }
</style>