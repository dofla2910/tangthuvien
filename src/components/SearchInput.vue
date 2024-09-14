<template lang="pug">
  form.search-wrapper(action="#" method="post")
    input.search-wrapper__input(type="text" name="search" id="search" placeholder="Search...")
    label.search-wrapper__label(for="search")
    button.search-wrapper__button(type='button') 
      FontAwesomeIcon(:icon='faSearch' class='search-wrapper__icon')
</template>

<script setup>
  import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';
  import { faSearch } from '@fortawesome/free-solid-svg-icons';
</script>

<style lang="scss" scoped>
  .search-wrapper {
    width: 100%;
    position: relative;
    display: inline-flex;
    align-items: center;
    background: white;

    &__input {
      flex: 1;
      height: 40px;
      font-size: 14px;
      padding: 0 11px 0 4px;
    }

    &__button {
      font-size: 20px;
      margin-right: 10px;
    }

    /*Smart phone nhỏ*/
    @media (min-width: 240px) {}

    /*Smart phone nhỏ*/
    @media (min-width: 240px) {}

    /*Iphone(480 x 640)*/
    @media (min-width: 320px) {}

    /*Tablet nhỏ(480 x 640)*/
    @media (min-width: 480px) {}

    /*Ipad dọc(768 x 1024)*/
    @media (min-width: 768px) {

      &__input {
        font-size: 24px;
        height: 48px;
        padding-left: 20px;
      }

      &__button {
        height: 100%;
        aspect-ratio: 1 / 1;
        color: #fff;
        font-size: 25px;
        line-height: 1;
        background-color: #3e98a1;
        margin-right: 0px;
      }
    }


    /*Ipad ngang(1024 x 768)*/
    @media (min-width: 1024px) {

      &__input {
        font-size: 30px;
        height: 80px;
        padding-left: 20px;
      }
    }
  }
</style>