<template lang="pug">
  .block-hots
    .block-hots__header
      h3.block-hots__title Truyện xem nhiều
      a.block-hots__more(href='#')
        span Xem thêm
        FontAwesomeIcon(:icon='faAngleRight')
    .block-hots_list
      BookList(:items='items')
</template>

<script setup>
  import { faAngleRight } from '@fortawesome/free-solid-svg-icons';
  import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';
  import BookList from './BookList.vue';

  //fetch data of top 6 books
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
  ]
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
      width: .75rem;
      height: 1.5em;
      vertical-align: middle;
      color: transparent;
      border-left: .2rem solid #ed424b;
    }

    &__more * {
      font-size: 14px;
      font-weight: 700;
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