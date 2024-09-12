<template lang="pug">
  nav.navbar
    ul.navbar__list
      li.navbar__item
        img.navbar__item-icon(src='/src/assets/images/category.png', alt='')
        span Thể loại
      //- li.navbar__item
      //-   span Diễn đàn
      li.navbar__item
        img.navbar__item-icon(src='/src/assets/images/ranking.png', alt='')
        span Bảng xếp hạng
      li.navbar__item
        img.navbar__item-icon(src='/src/assets/images/filter.png', alt='')
        span Bộ lọc
      li.navbar__item
        img.navbar__item-icon(src='/src/assets/images/reviews.png', alt='')
        span Reviews
      li.navbar__item
        img.navbar__item-icon(src='/src/assets/images/sprite.png', alt='')
        span Cửa hàng
      
</template>

<script setup>

</script>

<style lang="scss" scoped>
  .navbar {
    padding: 12px;
    background: white;

    &__list {
      width: 100%;
      display: inline-flex;
    }

    &__item {
      text-align: center;
      padding: 0 5px;
      width: 20%;
    }

    &__item span {
      font-size: 12px;
      font-weight: 500;
    }

    &__item-icon {
      width: 30px;
      height: 30px;
      margin: 0 auto;
    }
  }
</style>