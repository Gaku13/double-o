<template lang="pug">
  section#flow
    .container
      h1
        | Flow
        span ご相談の流れ
      ol.flow-container
        li.flow-card
          .content
            .inner
              button
                IconArrow
              .title 無料相談のご予約
              .text
                a( href="https://" target="_blank" rel="noopener noreferrer nofollow" ) 「お問い合わせフォーム」
                | にてご連絡ください。
                br
                | ３営業日以内に折り返しご連絡さしあげます。
                br
                | その際ご希望の日時をご指定ください。
                br
                | お電話、対面、ビデオ会議システムでのWeb相談のいずれかでご選択できます。
        li.flow-card( v-parallax="0.1" )
          .content
            .inner
              .title ご相談
              .text
                | 初回のご相談では現状の確認と、お客様のご要望についてヒアリングさせていただきます。
        li.flow-card
          .content
            .inner
              .title ご提案
              .text
                | ご提供いただいた情報をもとにお客様にとって最良の資産運用プランをご提案いたします。
                br
                | 契約がスタートしてからも継続して進捗を共有させていただきます。
                br
                | 報酬体系についてもここでご説明いたします。
        li.flow-card( v-parallax="0.1" )
          .content
            .inner
              .title 資産の見直し・メンテナンス
              .text
                | 個人の事情・経済情勢の変化に柔軟に対応するために、中長期で資産の定期的な見直し・メンテナンスをさせていただきます。
                br
                | 当社は強引な勧誘や意味のない見直しなどの提案は一切いたしません。

</template>
<i18n>
  {
    "ja": {},
    "en": {}
  }
</i18n>

<style lang="stylus" scoped>
section#flow
  padding 200px 0

h1
  margin-bottom 160px
  color $primary
  font-size 80px
  font-weight 300
  text-align center
  span
    display block
    margin 35px auto 0
    color $text
    font-size 20px
    font-weight normal

ol.flow-container
  display flex
  flex-wrap wrap
  list-style none
  margin 0 -4.16665vw
  li.flow-card
    position relative
    flex 0 1 50%
    width 50%
    padding 0 4.16665vw
    margin-bottom 200px
    color $textContrast
    counter-increment inst
    &::before
      position relative
      display block
      content ''
      padding-top 100%
      background-image url('/images/misc/bg-flow1.jpg')
      background-size cover
    &::after
      position absolute
      top -100px
      left calc(4.16665vw + 60px)
      content counter(inst)
      color $primary
      font-size 160px
      font-weight 300
      z-index 2
    .content
      display flex
      align-items center
      position absolute
      top 0
      left 4.16665vw
      right 4.16665vw
      bottom 0
      padding 60px
      z-index 1
      button
        position absolute
        top 30px
        right 30px
        width 60px
        height 60px
        background $primary
        border 0
        outline 0
        svg
          transition transform .25s ease-in-out
        &:hover
          svg
            transform rotate(45deg)
      a
        color $textContrast
        text-decoration underline
    &:nth-child(2)
      margin-top 50px
      &::before
        background-image url('/images/misc/bg-flow2.jpg')
    &:nth-child(3)
      margin-top 0
      &::before
        background-image url('/images/misc/bg-flow3.jpg')
    &:nth-child(4)
      margin-top 50px
      &::before
        background-image url('/images/misc/bg-flow4.jpg')

.title
  margin-bottom 30px
  font-size 20px
  font-weight 600

.text
  line-height 32px

</style>

<script>
import IconArrow from '~/static/images/icon/arrow.svg?inline'

export default {
  components: {
    IconArrow,
  }
}
</script>
