<template lang="pug">
  section#about
    .data-box
      h1 About
      .info
        p
          | ダブルオーキャピタル株式会社
          | 静岡県裾野市深良153-5-103

          | 代表
          | 大庭 宏之
      .career
        .row
          .col
            | 2006年
          .col
            | 東京理科大学工学部電気工学科　卒業 
        .row
          .col
            | 2006年
          .col
            | 野村證券　入社
            | 大阪・東京・神奈川・静岡にて個人および法人の資産運用コンサルティングを担当
        .row
          .col
            | 2021年
          .col
            | ダブルオーキャピタル　設立
        .row
          .col
            | 資格
          .col
            | プライマリープライベートバンカー
            | （公益社団法人　日本証券アナリスト協会）

    .image-box
      .image
        img( src="/images/misc/gov.jpg" alt="社長" )
      a( href="https://" target="_blank" rel="noopener noreferrer nofollow" )
        .arrow
          IconArrow
        .content
          .en Contact
          .jp お問い合わせ

</template>
<i18n>
  {
    "ja": {},
    "en": {}
  }
</i18n>

<style lang="stylus" scoped>
</style>

<script>
import IconArrow from '~/static/images/icon/arrow.svg?inline'

export default {
  components: {
    IconArrow
  }
}
</script>
