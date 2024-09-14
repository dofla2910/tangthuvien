<template lang="pug">
  .block-update
    .block-update__header
      h3.block-update__title Truyện mới cập nhật
      a.block-update__more(href='#')
        span Xem thêm
        FontAwesomeIcon(:icon='faAngleRight')
    .block-update__nav
      a.block-update__nav-item.active(href='#' @click='(e) => changeTab(e, 1)') Convert
      a.block-update__nav-item(href='#' @click='(e) => changeTab(e, 2)') Dịch
      a.block-update__nav-item(href='#' @click='(e) => changeTab(e, 3)') Ngôn tình
    .block-update__tab-list
      BookList(:items='items')
    .block-update__tab-list.disabled
      BookList(:items='items.map((item, i, items) => items[items.length - 1 - i])')
    .block-update__tab-list.disabled
      BookList(:items='items')
</template>

<script setup>
  import { faAngleRight } from '@fortawesome/free-solid-svg-icons';
  import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';
  import BookList from './BookList.vue';

  const changeTab = (e, tab) => {
    e.preventDefault();
    const nav = document.querySelectorAll('.block-update__nav-item');
    nav.forEach((item) => {
      item.classList.remove('active');
    })
    nav[tab - 1].classList.add('active');
    const list = document.querySelectorAll('.block-update__tab-list');
    list.forEach((item) => {
      item.classList.add('disabled');
    });
    list[tab - 1].classList.remove('disabled');
  }

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

  .block-update {
    width: 100%;
    padding: 6px;
    background-color: #fff;

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

    &__nav {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 1px;
      border: 1px solid #ed424b;
      border-radius: 10px;
      overflow: hidden;
    }

    &__nav-item {
      position: relative;
      font-weight: 400;
      font-size: 16px;
      padding: 5px 0;
      text-align: center;
      color: #ed424b;
      text-decoration: none;
    }

    &__nav-item+&__nav-item::before {
      content: '';
      position: absolute;
      left: -1px;
      top: 0;
      height: 100%;
      width: 1px;
      background-color: #ed424b;
    }

    &__nav-item.active {
      background-color: #ed424b;
      color: #fff;
    }

    &__nav-item:hover {
      background-color: #ed424b;
      color: #fff;
    }

    &__nav-item:not(.active):hover::before,
    &__nav-item:hover+&__nav-item.active::before {
      background-color: #fff;
    }

    &__tab-list {
      width: 100%;
      transition: display 1s ease-in-out;

      &.disabled {
        display: none;
      }
    }

    /*Ipad dọc(768 x 1024)*/
    @media (min-width: 768px) {
      &__header {
        height: 3.5rem;
      }

      &__title,
      &__nav-item {
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

      &__title,
      &__nav-item {
        font-size: 30px;
      }

      &__more * {
        font-size: 28px;
      }
    }

    @media (min-width: 1200px) {
      &__header {
        height: 2.75rem;
      }

      &__title,
      &__nav-item {
        font-size: 20px;
      }

      &__more * {
        font-size: 14px;
      }
    }
  }


  //responsive

  // @media (min-width: 1024px) {
  //   .header {

  //     &__title {
  //       font-size: 30px;
  //     }

  //     &__more * {
  //       font-size: 28px;
  //     }
  //   }

  //   .nav {

  //     &__item {
  //       font-size: 30px;
  //     }
  //   }
  // }
</style>