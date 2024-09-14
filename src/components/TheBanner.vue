<template lang="pug">
  .banner
    .banner__inner
      a(href='/tai-app')
        img(src='/src/assets/images/banner.jpg', alt='')
</template>

<script setup>

</script>

<style lang="scss" scoped>
  .banner {
    max-width: 100%;

    &__inner {
      margin: 3% auto;
      width: 100%;

      img {
        max-width: 100%;
        object-fit: cover;
      }
    }
  }
</style>