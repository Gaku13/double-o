<template lang="pug">
  section#hero
    .bg-container
      .bg.bg1
        .typo
          h1
            | 持続可能な資産運用を
            br
            | 誠実にサポート
      //- agile( :options="swiperOption" )
        .bg.bg1
          .typo
            h1
              | 持続可能な資産運用を
              br
              | 誠実にサポート
        .bg.bg2
          .typo
            .tagline
              | 一生涯マンツーマン型
        .bg.bg3
          .typo
            .tagline
              | 最新のマネートレンド
        .bg.bg4
          .typo
            .tagline
              | 継続的な価値ある提案
      .button
        nuxt-link( v-scroll-to="'#contact'" to )
          .icon
            IconArrow
          .text
            | お問い合わせ

    .card-list
      .card( @mouseover="" )
        .content
          img( src="/images/icon/umbrella.svg" )
          .text
            | 安心
            span with strong security
      .card( @mouseover="" )
        .content
          img( src="/images/icon/timer.svg" )
          .text
            | 最新
            span resourceful information
      .card( @mouseover="" )
        .content
          img( src="/images/icon/roadmap.svg" )
          .text
            | 継続
            span continuous support

</template>
<i18n>
  {
    "ja": {},
    "en": {}
  }
</i18n>
<script>
import IconArrow from '~/static/images/icon/arrow.svg?inline'

export default {
  components: {
    IconArrow
  },
  data () {
    return {
      swiperOption: {
        fade: true,
        autoplay: true,
        navButtons: false
      }
    }
  },
  methods: {
  }
}
</script>

<style lang="stylus" scoped>
#hero
  display flex
  min-height calc(100vh - 80px)
  @media (max-width: 767px)
    flex-wrap wrap
.bg-container
  position relative
  width 66.6666vw
  @media (max-width: 767px)
    width 100%
    height calc(75vh - 80px)
  .bg
    position absolute
    top 0
    left 0
    right 0
    bottom 0
    padding 40px
    background-image url('/images/misc/bg-slice1.jpg')
    background-size cover
    background-position center center
    @media (max-width: 639px)
      padding 20px
    &.bg2
      background-image url('/images/misc/bg-slice2.jpg')
    &.bg3
      background-image url('/images/misc/bg-slice3.jpg')
    &.bg4
      background-image url('/images/misc/bg-slice4.jpg')
    &.bg2, &.bg3, &.bg4
      display flex
      align-items center
      justify-content center
      padding-bottom 100px
      .typo
        padding-bottom 30px
        border-bottom 1px solid $primary
  .typo
    h1
      display inline-block
      padding-bottom 40px
      color $white
      font-size 48px
      font-weight 300
      border-bottom 1px solid $primary
      @media (max-width: 1279px)
        font-size 40px
      @media (max-width: 1023px)
        font-size 32px
      @media (max-width: 639px)
        font-size 24px
  .tagline
    color $textContrast
    font-size 32px
    font-weight normal
    text-align center
  .button
    position absolute
    left 40px
    bottom 50px
    z-index 9999
    @media (max-width: 639px)
      left 20px
      bottom 30px
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
      @media (max-width: 639px)
        width 44px
        height 44px
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
      @media (max-width: 639px)
        width 160px
        height 44px

.card-list
  width 33.3333vw
  @media (max-width: 767px)
    display flex
    align-items center
    justify-content center
    flex-wrap wrap
    width 100%
    height 25vh
  @media (max-width: 639px)
    height auto
  .card
    position relative
    width 100%
    height 33.3333%
    color $white
    background-color $black
    border-bottom 1px solid $whiteTransparent2
    overflow hidden
    @media (max-width: 767px)
      width 33.333vw
      height 100%
    @media (max-width: 639px)
      width 100vw
      height auto
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
      @media (max-width: 639px)
        padding 20px
    img
      width 120px
      height 120px
      @media (max-width: 1279px)
        width 100px
        height 100px
      @media (max-width: 767px)
        width 60px
        height 60px
        align-self flex-start
      @media (max-width: 639px)
        width 44px
        height 44px
    .text
      align-self flex-end
      font-size 32px
      text-align right
      letter-spacing .1rem
      @media (max-width: 1279px)
        font-size 28px
      @media (max-width: 767px)
        font-size 20px
      span
        display block
        color $textContrastMuted
        font-size 18px
        @media (max-width: 1279px)
          font-size 16px
        @media (max-width: 767px)
          font-size 14px
</style>