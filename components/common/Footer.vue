<template lang="pug">
  footer#contact
    .logo
      Logo
    .nav
      ul
        li
          nuxt-link( v-scroll-to="mission" to ) Mission
        li
          nuxt-link( v-scroll-to="value" to ) Value
        li
          nuxt-link( v-scroll-to="service" to ) Service
        li
          nuxt-link( v-scroll-to="about" to ) About
        li
          a( href="https://" target="_blank" rel="noopener noreferrer nofollow" ) Contact
      .copyright
        | © Double O Capital.Ltd

</template>

<style lang="stylus">
footer
  position relative
  z-index 1
</style>

<script>
import Logo from '~/static/images/logo.svg?inline'

export default {
  components: {
    Logo,
  },
  data() {
    return {
      mission: {
        el: '#mission',
        onStart: function(el) {
          var nav;
          nav = document.querySelector('.nav-container');
          return nav.classList.remove('show');
        }
      },
      value: {
        el: '#value',
        onStart: function(el) {
          var nav;
          nav = document.querySelector('.nav-container');
          return nav.classList.remove('show');
        }
      },
      service: {
        el: '#service',
        onStart: function(el) {
          var nav;
          nav = document.querySelector('.nav-container');
          return nav.classList.remove('show');
        }
      },
      about: {
        el: '#about',
        onStart: function(el) {
          var nav;
          nav = document.querySelector('.nav-container');
          return nav.classList.remove('show');
        }
      }
    }
  }
}
</script>
