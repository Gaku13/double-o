<template lang="pug">
  footer#contact( v-scroll="footer" )
    .container
      .footer-content
        a.typo( href="https://" target="_blank" @mouseover="mouseover" @mouseleave="mouseleave" rel="noopener noreferrer nofollow" )
          | Contact us
</template>

<style lang="stylus">
footer
  position: relative
  margin-top: 300px
  overflow: hidden
  z-index: 0
  &:after
    content: ''
    position: absolute
    background-color: $primary
    top: 0
    left: 0
    right: 0
    bottom: 0
    transition: transform .8s .25s ease, background-color 1s ease
    transform: translateY(100%)
    z-index: 0
  &.onmouse
    &:after
      background-color: $white
  .footer-content
    position: relative
    padding: 160px 0
    text-align: center
    z-index: 1
  a.typo
    color: $muted
    font-size: 44px
    transition: color .1s 0s
body.footer--show
  footer
    &:after
      transform: translateY(0)
    a.typo
      color: $white
      &:hover
        color: $primary
</style>

<script>
export default {
  methods: {
    footer: function(evt, el) {
      var body, pos;
      body = document.querySelector('body');
      pos = el.getBoundingClientRect().top + window.pageYOffset - window.innerHeight;
      pos = pos + 250;
      if (window.scrollY > pos) {
        return body.classList.add('footer--show');
      } else if (window.scrollY < pos) {
        return body.classList.remove('footer--show');
      }
    },
    mouseover: function() {
      var footer;
      footer = document.querySelector('footer');
      return footer.classList.add('onmouse');
    },
    mouseleave: function() {
      var footer;
      footer = document.querySelector('footer');
      return footer.classList.remove('onmouse');
    }
  }
}
</script>
