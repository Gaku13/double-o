<template lang="pug">
  main.home
    section#hero
      .bg-container
        .typo
          h1
            | 持続可能な資産運用を
            br
            | 誠実にサポート
        .button
          nuxt-link( v-scroll-to="'#contact'" to )
            .icon
              IconArrow
            .text
              | お問い合わせ

      .card-list
        button.card
          .content
            img( src="/images/icon/umbrella.svg" )
            .text
              | 安心
              span with strong security
        button.card
          .content
            img( src="/images/icon/timer.svg" )
            .text
              | 最新
              span resourceful information
        button.card
          .content
            img( src="/images/icon/roadmap.svg" )
            .text
              | 継続
              span continuous support
    Mission
    Value
    Service
    Flow
    About
</template>

<i18n>
  {
    "ja": {},
    "en": {}
  }
</i18n>

<script>
import Mission from '~/components/home/Mission.vue'
import Value from '~/components/home/Value.vue'
import Service from '~/components/home/Service.vue'
import Flow from '~/components/home/Flow.vue'
import About from '~/components/home/About.vue'

import IconArrow from '~/static/images/icon/arrow.svg?inline'

export default {
  components: {
    Mission,
    Value,
    Service,
    Flow,
    About,
    IconArrow,
  }
  /*,
  computed: {
    availableLocales () {
      return this.$i18n.locales.filter(i => i.code !== this.$i18n.locale)
    }
  }
  */
};
</script>

<style lang="stylus" scoped>
.home
  padding-top 80px
  /*
  @media (max-width: 1500px)
    padding-top 200px
  @media (max-width: 750px)
    padding-top: 100px */
  .page.is-loaded &
    .typo, .content
      transform translateY(0)
      opacity 1

#hero
  display flex
  min-height calc(100vh - 80px)

.bg-container
  position relative
  width 66.6666vw
  padding 40px
  background-image url('/images/misc/bg-slice1.jpg')
  background-size cover
  // background-position right center
  .typo
    h1
      display inline-block
      padding-bottom 40px
      color $white
      font-size 48px
      font-weight 300
      border-bottom 1px solid $primary
  .button
    position absolute
    left 40px
    bottom 50px
    a
      display flex
      align-items center
      &:hover
        svg
          transform rotate(45deg)
    .icon
      width 60px
      height 60px
      display flex
      align-items center
      justify-content center
      background-color $black
      svg
        transition transform .25s ease-in-out
    .text
      display flex
      align-items center
      justify-content center
      color $white
      width 200px
      height 60px
      background-color $red

.card-list
  width 33.3333vw
  button.card
    position relative
    width 100%
    height 33.3333%
    color $white
    background-color $black
    border 0
    border-bottom 1px solid $whiteTransparent2
    outline 0
    overflow hidden
    cursor pointer
    &:before
      content ''
      position absolute
      top 0
      left 0
      background-color $primary
      width 100%
      height 100%
      transition transform .4s ease-in-out
      transform translateY(100%)
      z-index 0
    &:hover
      &:before
        transform translateY(0)
    &:last-child
      border 0
    .content
      position relative
      width 100%
      height 100%
      display flex
      align-items center
      justify-content space-between
      padding 40px
    img
      width 120px
      height 120px
    .text
      align-self flex-end
      font-size 32px
      text-align right
      letter-spacing .1rem
      span
        display block
        color $textContrastMuted
        font-size 18px
</style>