<template lang="pug">
  header.header
    a.header__logo(href='/')
      span Tàng thư viện
      img.header__logo-image(src='/src/assets/images/logo.png', alt='')

    a.header__forum(href='/forum')
      p Diễn đàn

    SearchInput(class="header__search")

    .header__side
      a.header__app(href='/')
        FontAwesomeIcon(:icon='faDownload', class="header__app-icon")
        span App
      a.header__account(href='/login')
        FontAwesomeIcon(:icon='faUser')
          span Account

    //- HomeSlide

    //- SearchBar

    //- HomeNav
</template>

<script setup>
  import { faDownload } from '@fortawesome/free-solid-svg-icons';
  import { faUser } from '@fortawesome/free-regular-svg-icons';
  import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';
  import SearchInput from './SearchInput.vue';
</script>

<style lang="scss" scoped>
  .header {
    display: grid;
    grid-template-columns: auto auto 1fr;
    column-gap: 15px;
    row-gap: 15px;
    width: 100%;
    padding: 12px;

    &__logo {
      display: inline-flex;
      align-items: center;
      order: 1;
      font-weight: 500;
      cursor: pointer;
    }

    &__logo span {
      font-size: 17px;
      font-weight: 500;
    }

    &__logo-image {
      display: none;
      height: 52px;
    }

    &__forum {
      display: inline-flex;
      align-items: center;
      justify-content: flex-end;
      font-size: 13px;
      font-weight: 100;
      line-height: 1.5rem;
      text-align: center;
      color: #ed424b;
      order: 2;
      border: 1px solid #ed424b;
      border-radius: 4px;
      padding: 3px 12px;
    }

    &__side {
      flex: 1;
      display: inline-flex;
      justify-content: flex-end;
      order: 3;
    }

    &__app {
      display: inline-flex;
      align-items: center;
      background: #3e98a1;
      color: #fff;
      font-size: 13px;
      padding: 4px 10px;
      border-radius: 5px;
      margin-right: 10px;
    }

    &__app-icon {
      margin-right: 5px;
    }

    &__account {
      display: flex;
      align-items: center;
      color: #ed424b;
    }

    &__search {
      order: 4;
      grid-column: 1 / 4;
    }

    /*Ipad dọc(768 x 1024)*/
    @media (min-width: 768px) {
      padding: 18px;

      &__logo span {
        font-size: 30px;
      }

      &__app,
      &__forum,
      &__account {
        font-size: 24px
      }

      &__search {
        margin: 0;
        border: 1px solid #dbdbdb;
      }
    }

    /*Ipad ngang(1024 x 768)*/
    @media (min-width: 1024px) {
      row-gap: 30px;

      &__app,
      &__forum,
      &__account {
        font-size: 30px
      }

      &__logo span {
        display: none;
      }

      &__logo-image {
        display: inline-block;
        height: 70px;
      }
    }

    @media (min-width: 1200px) {}
  }

</style>