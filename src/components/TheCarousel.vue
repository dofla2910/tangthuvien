<template lang="pug">
  Carousel(
    :transition="500",
    wrapAround
  )
    Slide(
      v-for="image in imageList",
      :key="image.id"
    )
      a.carousel__image(href="#" @click.prevent="() => {}")
        img(
          :src="image.src",
          alt=""
        )
    template(#addons)
      Pagination
</template>

<script setup>
  import { Carousel, Pagination, Slide } from 'vue3-carousel'
  import 'vue3-carousel/dist/carousel.css'

  const imageList = [
    {
      id: 1,
      src: 'https://truyen.tangthuvien.vn/images/slide3.jpg'
    },
    {
      id: 2,
      src: 'https://truyen.tangthuvien.vn/images/slide7.jpg'
    },
    {
      id: 3,
      src: 'https://truyen.tangthuvien.vn/images/slide3.jpg'
    },
    {
      id: 4,
      src: 'https://truyen.tangthuvien.vn/images/slide7.jpg'
    },
    {
      id: 5,
      src: 'https://truyen.tangthuvien.vn/images/slide3.jpg'
    },
    {
      id: 6,
      src: 'https://truyen.tangthuvien.vn/images/slide7.jpg'
    },
    {
      id: 7,
      src: 'https://truyen.tangthuvien.vn/images/slide3.jpg'
    },
    {
      id: 8,
      src: 'https://truyen.tangthuvien.vn/images/slide7.jpg'
    },
    {
      id: 9,
      src: 'https://truyen.tangthuvien.vn/images/slide3.jpg'
    },
    {
      id: 10,
      src: 'https://truyen.tangthuvien.vn/images/slide7.jpg'
    },
  ]
</script>

<style lang="scss" scoped>
  .carousel {
    width: 100%;

    &__image {
      padding: 0 12px;
      width: 100%;
      height: 100%;
      cursor: pointer;
    }

    &__image img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    &__pagination {
      position: absolute;
      left: 50%;
      transform: translateX(-50%);
      margin-top: -20px;
    }
  }
</style>