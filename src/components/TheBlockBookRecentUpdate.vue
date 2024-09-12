<template lang="pug">
  .block-update
    .header
      h3.header__title Truyện mới cập nhật
      a.header__more(href='#')
        span Xem thêm
        FontAwesomeIcon(:icon='faAngleRight')
    .tab
      nav.nav
        a.nav__item.active(href='#' @click='(e) => changeTab(e, 1)') Convert
        a.nav__item(href='#' @click='(e) => changeTab(e, 2)') Dịch
        a.nav__item(href='#' @click='(e) => changeTab(e, 3)') Ngôn tình
    .tab-1.tab-list
      BookList
    .tab-2.tab-list.disabled
      BookList
    .tab-3.tab-list.disabled
      BookList
</template>

<script setup>
  import { faAngleRight } from '@fortawesome/free-solid-svg-icons';
  import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';
  import BookList from './BookList.vue';

  const changeTab = (e, tab) => {
    e.preventDefault();
    const nav = document.querySelectorAll('.nav__item');
    nav.forEach((item) => {
      item.classList.remove('active');
    })
    nav[tab - 1].classList.add('active');
    const list = document.querySelectorAll('.tab-list');
    list.forEach((item) => {
      item.classList.add('disabled');
    });
    list[tab - 1].classList.remove('disabled');
  }
</script>

<style lang="scss" scoped>
  .block-update,
  .tab {
    width: 100%;
    padding: 6px;
    background-color: #fff;
  }

  .header {
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

    &__title {
      font-weight: 400;
      display: inline;
      font-size: 16px;
    }

    &__title::before {
      content: '';
      display: inline-block;
      width: .6rem;
      height: 1em;
      vertical-align: middle;
      color: transparent;
      border-left: 2px solid #ed424b;
    }

    &__more * {
      font-size: 14px;
      font-weight: 700;
    }
  }

  .nav {
    display: flex;
    width: 100%;
    margin: 0 auto;

    &__item {
      font-weight: 400;
      font-size: 13px;
      padding: 5px 5px;
      text-align: center;
      color: #ed424b;
      border: 1px solid #ed424b;
      float: left;
      width: 33.3333%;
      text-decoration: none;

      &+& {
        border-left-width: 0;
      }

      &:first-child {
        border-radius: 4px 0 0 4px;

      }

      &:last-child {
        border-radius: 0 4px 4px 0;
      }
    }

    &__item.active {
      background-color: #ed424b;
      color: #fff;
    }
  }

  .tab-list {
    width: 100%;

    &.disabled {
      display: none;
    }
  }
</style>