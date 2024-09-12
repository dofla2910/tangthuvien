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

  // const props = defineProps({
  //   item: {
  //     type: Object,
  //     required: true
  //   }
  // })

  const items = [
    {
      id: 1,
      image: 'https://nae.vn/ttv/ttv/public/images/story/b574c544335443cc763f3702d598d50b96124d4ea630dd4bfbad677c68892090.jpg',
      title: 'Trận Vấn Trường Sinh',
      category: 'Tiên Hiệp',
      author: 'Quan Hư',
      totalView: 153408,
      totalChapter: 830,
      status: 'Chưa hoàn thành',
    },
    {
      id: 2,
      image: 'https://nae.vn/ttv/ttv/public/images/story/877d54f5b01cedf5da631af873e80e3af9cf4f32fb09c8d6237f7193ccf8dacf.jpg',
      title: '[Dịch] Kiếm Lai - Tàng Thư Viện',
      category: 'Tiên Hiệp',
      author: 'Phong Hỏa Hí Chư Hầu',
      totalView: 1094187,
      totalChapter: 434,
      status: 'Chưa hoàn thành',
    },
    {
      id: 3,
      image: 'https://nae.vn/ttv/ttv/public/images/story/99d2aa117de6f54b06b64cbbebef2b435336977dfee71f2ee5766d48b31734f3.jpg',
      title: 'Luân Hồi Lạc Viên',
      category: 'Đồng Nhân',
      author: 'Na Nhất Chích Văn Tử ',
      totalView: 3720923,
      totalChapter: 4206,
      status: 'Chưa hoàn thành',
    },
    {
      id: 4,
      image: 'https://nae.vn/ttv/ttv/public/images/story/f7cd2067ca3da64d4a9e6b1545d2b5c23b1f55aaf8f353a2958fc9bf466b28b2.jpg',
      title: 'Vô Thượng Thiên Tôn',
      category: 'Huyền Huyễn',
      author: 'Khai Hoang ',
      totalView: 146045,
      totalChapter: 272,
      status: 'Chưa hoàn thành',
    },
    {
      id: 5,
      image: 'https://nae.vn/ttv/ttv/public/images/story/6e839eb1100bc58db13f065420c2cbce3c1840ab6881fe979dbf5e7e4a483724.jpg',
      title: 'Tinh Không Chức Nghiệp Giả',
      category: 'Khoa Huyễn',
      author: 'Văn Sao Công',
      totalView: 65006,
      totalChapter: 186,
      status: 'Chưa hoàn thành',
    },
    {
      id: 6,
      image: 'https://nae.vn/ttv/ttv/public/images/story/6e839eb1100bc58db13f065420c2cbce3c1840ab6881fe979dbf5e7e4a483724.jpg',
      title: 'Tinh Không Chức Nghiệp Giả',
      category: 'Khoa Huyễn',
      author: 'Văn Sao Công',
      totalView: 65006,
      totalChapter: 186,
      status: 'Chưa hoàn thành',
    }
  ]
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