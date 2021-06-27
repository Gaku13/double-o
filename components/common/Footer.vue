<template lang="pug">
  footer#contact
    .logo
      Logo
    .nav
      ul
        li
          nuxt-link( v-scroll-to="mission" to="/#mission" ) Mission
        li
          nuxt-link( v-scroll-to="value" to="/#value" ) Value
        li
          nuxt-link( v-scroll-to="service" to="/#service" ) Service
        li
          nuxt-link( v-scroll-to="about" to="/#about" ) About
        li
          a( href="https://" target="_blank" rel="noopener noreferrer nofollow" ) Contact
      .copyright
        | ©Double O Capital.Ltd

</template>

<style lang="stylus">
</style>

<script>
import Logo from '~/static/images/logo.svg?inline'

export default {
  components: {
    Logo,
  },
}
</script>
