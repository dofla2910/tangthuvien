<template lang="pug">
  .item
    a(href="/book-detail" @click.prevent="() => {}")
      .item__image
        img(:src="props.item.image", alt="")
      .item__detail
        h4 {{ props.item.title }}
        p.gr-info Thể loại: {{ props.item.category }}
        p.gr-info Tác giả: {{ props.item.author }}
        p.gr-more Lượt xem: {{ props.item.totalView }}
        p.gr-more Số chương: {{ props.item.totalChapter }}
        p.gr-more Tình trạng: {{ props.item.status }}
</template>

<script setup>
  const props = defineProps({
    item: {
      type: Object,
      required: true
    }
  })
</script>

<style lang="scss" scoped>
  .item {
    width: 100%;
    height: 100%;

    a {
      display: flex;
    }

    &__image {
      width: 30%;
    }

    &__image img {
      width: 100%;
    }

    &__detail {
      flex: 1;
      padding-left: 10px;
      padding-right: 20px;
      font-size: 12px;
    }

    &__detail h4 {
      width: 100%;
      font-size: 14px;
      font-weight: 700;
      margin-bottom: 5px;
      text-overflow: ellipsis;
    }

    &__detail p {
      margin: 3px 0 2px;
      text-overflow: ellipsis;
      overflow: hidden;
      font-weight: 100;
    }

    &__detail .gr-info {
      color: #969ba3;
    }

    @media (min-width: 768px) {
      &__image {
        width: 40%;
      }

      &__detail {
        font-size: 16px;
      }

      &__detail h4 {
        font-size: 20px;
      }
    }

    @media (min-width: 1024px) {
      padding: 25px;

      &__image {
        width: 25%;
      }

      &__detail {
        padding-left: 40px;
        padding-right: 25px;
        font-size: 28px;
      }

      &__detail h4 {
        font-size: 36px;
      }
    }

    @media (min-width: 1200px) {
      padding: 0;

      &__image {
        width: 25%;
      }

      &__detail {
        padding-left: 10px;
        padding-right: 10px;
        font-size: 10px;
      }

      &__detail h4 {
        font-size: 12px;
      }
    }
  }
</style>