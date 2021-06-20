<template lang="pug">
  header
    nuxt-link.logo_type( to="/" )
      Logo
    nav
      a.nav-button( href="#" @click="click" )
        | menu
      .nav-container
        a.nav-close( href="#" @click="close" )
          X
        ul
          li
            nuxt-link( v-scroll-to="service" to="/#service" ) Service
          li
            nuxt-link( v-scroll-to="about" to="/#about" ) About
          li
            nuxt-link( v-scroll-to="contact" to ) Contact
</template>

<script>
import Logo from '~/static/images/logo.svg?inline'
import X from '~/static/images/icon/x.svg?inline'

export default {
  components: {
    Logo,
    X,
  },
  data: function() {
    return {
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
      },
      contact: {
        el: '#contact',
        onStart: function(el) {
          var nav;
          nav = document.querySelector('.nav-container');
          return nav.classList.remove('show');
        }
      }
    };
  },
  methods: {
    click: function() {
      var nav;
      nav = document.querySelector('.nav-container');
      return nav.classList.add('show');
    },
    close: function() {
      var nav;
      nav = document.querySelector('.nav-container');
      return nav.classList.remove('show');
    }
  }
}
</script>

<style lang="stylus">
  header
    position fixed
    top 50px
    left 50px
    right 50px
    transition transform .75s .25s ease, opacity .75s .25s ease, visibility .75s .25s
    transform translateY(10px)
    visibility hidden
    opacity 0
    z-index $zindex-header
    .page.is-loaded &
      transform translateY(0)
      opacity 1
      visibility visible
    @media (max-width: 750px)
      top 25px
      left 25px
      right 25px

  .logo_type
    img
      width 80px
      height auto
      @media (max-width: 750px)
        width 70px
  nav
    position absolute
    top 0
    right 0
    .nav-button
      display none
      visibility hidden
      font-weight 700
      letter-spacing .1rem
      @media (max-width: 750px)
        display block
        visibility visible
    .nav-container
      position relative
      visibility visible
      @media (max-width: 750px)
        position fixed
        top -25px
        right -25px
        width 100vw
        height 100vh
        background-color $primary
        transition transform .2s ease, visibility .2s ease
        transform translateX(100%)
        overflow-x hidden
        overflow-y auto
        visibility hidden
        &.show
          transform translateX(0)
          visibility visible
    .nav-close
      display none
      position absolute
      top 30px
      right 30px
      @media (max-width: 750px)
        display block
      img
        width 32px
        height 32px
    ul
      display flex
      align-items center
      justify-content center
      list-style none
      margin 0
      padding 0
      li
        padding 0 20px
        &.col-lang
          border-left 1px solid $text
          padding-left 40px
          margin-left 20px
          @media (max-width: 750px)
            position relative
            border 0
            padding 40px 20px 0
            margin 50px 0 0
            &::before
              content ''
              position absolute
              top -4px
              border-top 1px solid $text
              width 200px
        a
          color $text
          font-size 18px
          font-weight 700;
          text-decoration none
          transition color .3s
          @media (max-width: 1050px)
            font-size 16px
          &:hover
            color $primary
            @media (max-width: 750px)
              color $white
      @media (max-width: 750px)
        display block
        padding 80px 30px
        li
          margin-bottom 30px
          a
            font-size 24px
            font-weight 900
</style>

