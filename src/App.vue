<template lang="pug">
  LayoutDefault
    TheBanner
    TheCarousel
    TheBanner 
    TheBlockBookRecentUpdate
    TheBlockBookHots
    TheBlockBookNew
    TheBlockBookFinished
</template>

<script setup>
  import LayoutDefault from "./components/LayoutDefault.vue";
  import TheBanner from "./components/TheBanner.vue";
  import TheCarousel from "./components/TheCarousel.vue";
  import TheBlockBookRecentUpdate from "./components/TheBlockBookRecentUpdate.vue";
  import TheBlockBookHots from "./components/TheBlockBookHots.vue";
  import TheBlockBookNew from "./components/TheBlockBookNew.vue";
  import TheBlockBookFinished from "./components/TheBlockBookFinished.vue";
</script>

<style scoped></style>
