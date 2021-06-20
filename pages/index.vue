<template lang="pug">
  main.home
    .container
      section.home__main
        .typo
          | Yappy
        | YAPPY
        .content( v-parallax="0.15" )
          .desc
            h1 Nice
          div
            Link( v-scroll-to="'#service'" to )
              | Check out how
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
import Link from '~/components/common/Link.vue';
import Mission from '~/components/home/Mission.vue';
import Value from '~/components/home/Value.vue';
import Service from '~/components/home/Service.vue';
import Flow from '~/components/home/Flow.vue';
import About from '~/components/home/About.vue';

export default {
  components: {
    Link,
    Mission,
    Value,
    Service,
    Flow,
    About
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
  padding-top 250px
  @media (max-width: 1500px)
    padding-top 200px
  @media (max-width: 750px)
    padding-top: 100px

  .page.is-loaded &
    .typo, .content
      transform translateY(0)
      opacity 1

</style>