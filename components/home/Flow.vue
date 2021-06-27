<template lang="pug">
  section#flow
    h1
      | Flow
      span ご相談の流れ
    ol.flow-container
      li.flow-card
        .content
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

      li.flow-card
        .content
          .title ご相談
          .text
            | 初回のご相談では現状の確認と、お客様のご要望についてヒアリングさせていただきます。
      li.flow-card
        .content
          .title ご提案
          .text
            | ご提供いただいた情報をもとにお客様にとって最良の資産運用プランをご提案いたします。
            br
            | 契約がスタートしてからも継続して進捗を共有させていただきます。
            br
            | 報酬体系についてもここでご説明いたします。
      li.flow-card
        .content
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
</style>

<script>
import IconArrow from '~/static/images/icon/arrow.svg?inline'

export default {
  components: {
    IconArrow,
  }
}
</script>
