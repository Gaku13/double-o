<template lang="pug">
  .page( :class="{ 'is-loaded': dataLoadFinish }" )
    Header
    .nuxt-container
      Loading
      .bg-icon-container
        LogoSymbol
      .nuxt-body
        nuxt
      Footer
</template>

<style lang="stylus">
.bg-icon-container
  position fixed
  display flex
  align-items center
  justify-content center
  top 0
  left 0
  width 100%
  height 100%
  z-index 0
  svg
    width 3rem
    height auto
    path
      fill $primary
.nuxt-container
  position relative
  z-index 3
.nuxt-body
  position relative
  min-height 100vh
  z-index 1

</style>

<script>
import Header from '~/components/common/Header.vue';
import Footer from '~/components/common/Footer.vue';
import Loading from '~/components/common/Loading.vue';
import LogoSymbol from '~/static/images/logo-symbol.svg?inline'

export default {
  components: {
      Header,
      Footer,
      Loading,
      LogoSymbol,
  },
  data: function() {
    return {
      dataLoadFinish: false
    };
  },
  mounted: function() {
    var page;
    page = document.querySelector('.page');
    page.classList.add('is-loading');
    return this.$nextTick(function() {
      var _this;
      _this = this;
      return setTimeout(function() {
        _this.dataLoadFinish = true;
      }, 1500);
    });
  }
}
 </script>
