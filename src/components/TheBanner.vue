<template lang="pug">
  .banner
    a(href='/tai-app')
      img(src='/src/assets/images/banner.jpg', alt='')
</template>

<script setup>

</script>

<style lang="scss" scoped>
  .banner {
    max-width: 100%;
    margin: 20px 0;

    img {
      max-width: 100%;
      object-fit: cover;
    }
  }
</style>