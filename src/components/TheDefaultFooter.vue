<template lang="pug">
  footer.footer
    .footer__links
      a.footer__link(href='/ios-download') IOS
      a.footer__link(href='/android-download') Android
      a.footer__link(href='/') PC
      a.footer__link(href='/noi-quy') Nội quy
    .footer__copyright Copyright © 2017 Tàng thư viện
</template>

<script setup>

</script>

<style lang="scss" scoped>
  .footer {
    width: 100%;
    background-color: #fff;
    padding-bottom: 10px;

    &__links {
      display: flex;
      text-align: center;
      padding: 12px;
      border-top: 1px solid #f0f1f2;
    }

    &__link {
      flex: 1;
      line-height: 48px;
      color: #33373d;
      font-weight: 500;
      padding: 0 12px;
    }

    &__copyright {
      font-size: 13px;
      font-weight: 300;
      padding: 5px 0;
      text-align: center;
      color: #969ba3;
      margin-top: -20px;
    }
  }

</style>