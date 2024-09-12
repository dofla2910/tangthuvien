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

  // const props = defineProps({
  //   item: {
  //     type: Object,
  //     required: true
  //   }
  // })

  const items = [
    {
      id: 1,
      src: '/book',
      image: 'https://nae.vn/ttv/ttv/public/images/story/b574c544335443cc763f3702d598d50b96124d4ea630dd4bfbad677c68892090.jpg',
      title: 'Trận Vấn Trường Sinh',
    },
    {
      id: 2,
      src: '/book',
      image: 'https://nae.vn/ttv/ttv/public/images/story/877d54f5b01cedf5da631af873e80e3af9cf4f32fb09c8d6237f7193ccf8dacf.jpg',
      title: '[Dịch] Kiếm Lai - Tàng Thư Viện',
    },
    {
      id: 3,
      src: '/book',
      image: 'https://nae.vn/ttv/ttv/public/images/story/99d2aa117de6f54b06b64cbbebef2b435336977dfee71f2ee5766d48b31734f3.jpg',
      title: 'Luân Hồi Lạc Viên',
    },
    {
      id: 4,
      src: '/book',
      image: 'https://nae.vn/ttv/ttv/public/images/story/f7cd2067ca3da64d4a9e6b1545d2b5c23b1f55aaf8f353a2958fc9bf466b28b2.jpg',
      title: 'Vô Thượng Thiên Tôn',
    },
    {
      id: 5,
      src: '/book',
      image: 'https://nae.vn/ttv/ttv/public/images/story/6e839eb1100bc58db13f065420c2cbce3c1840ab6881fe979dbf5e7e4a483724.jpg',
      title: 'Tinh Không Chức Nghiệp Giả',
    },
    {
      id: 6,
      src: '/book',
      image: 'https://nae.vn/ttv/ttv/public/images/story/db460080ecb8d6af55606bb7870df6d5858553dcf44ddb59352ccb13db52ab41.jpg',
      title: 'Quỷ Tam Quốc'
    },
    {
      id: 1,
      src: '/book',
      image: 'https://nae.vn/ttv/ttv/public/images/story/b574c544335443cc763f3702d598d50b96124d4ea630dd4bfbad677c68892090.jpg',
      title: 'Trận Vấn Trường Sinh',
    },
    {
      id: 2,
      src: '/book',
      image: 'https://nae.vn/ttv/ttv/public/images/story/877d54f5b01cedf5da631af873e80e3af9cf4f32fb09c8d6237f7193ccf8dacf.jpg',
      title: '[Dịch] Kiếm Lai - Tàng Thư Viện',
    },
    {
      id: 3,
      src: '/book',
      image: 'https://nae.vn/ttv/ttv/public/images/story/99d2aa117de6f54b06b64cbbebef2b435336977dfee71f2ee5766d48b31734f3.jpg',
      title: 'Luân Hồi Lạc Viên',
    },
    {
      id: 4,
      src: '/book',
      image: 'https://nae.vn/ttv/ttv/public/images/story/f7cd2067ca3da64d4a9e6b1545d2b5c23b1f55aaf8f353a2958fc9bf466b28b2.jpg',
      title: 'Vô Thượng Thiên Tôn',
    },
    {
      id: 5,
      src: '/book',
      image: 'https://nae.vn/ttv/ttv/public/images/story/6e839eb1100bc58db13f065420c2cbce3c1840ab6881fe979dbf5e7e4a483724.jpg',
      title: 'Tinh Không Chức Nghiệp Giả',
    },
    {
      id: 6,
      src: '/book',
      image: 'https://nae.vn/ttv/ttv/public/images/story/db460080ecb8d6af55606bb7870df6d5858553dcf44ddb59352ccb13db52ab41.jpg',
      title: 'Quỷ Tam Quốc'
    },
  ]
</script>

<style lang="scss" scoped>
  .book-list {
    display: grid;
    grid-template-rows: 1fr;
    grid-template-columns: repeat(4, 1fr);
    gap: 12px;
    padding: 6px;
    margin-top: 6px;
    overflow-x: auto;

    &__item {
      width: 100%;
      margin-bottom: 12px;
    }

    @media (min-width: 768px) {
      grid-template-columns: repeat(4, 1fr);
    }

    @media (min-width: 1024px) {
      grid-template-columns: repeat(3, 1fr);
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