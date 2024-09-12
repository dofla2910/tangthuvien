<template lang="pug">
  TheDefaultHeader
  TheDefaultNavigationBar
  main
    slot
  TheDefaultFooter
</template>

<script setup>
  import TheDefaultHeader from './TheDefaultHeader.vue';
  import TheDefaultNavigationBar from './TheDefaultNavigationBar.vue';
  import TheDefaultFooter from './TheDefaultFooter.vue';
</script>

<style lang="scss" scoped></style>