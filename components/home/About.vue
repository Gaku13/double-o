<template lang="pug">
  section#about.home__about
    .recruitment
      .content( v-parallax="0.15" )
        .desc
          p
            | test
        div
          Link( href="https://" target="_blank" rel="noopener noreferrer nofollow" )
            | Check

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
import Link from '~/components/common/Link.vue';

export default {
  components: {
    Link
  }
}
</script>
