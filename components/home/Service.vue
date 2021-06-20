<template lang="pug">
  section#service.home__service
    .main-typo.typo
      | hey
    .services
      .order-num.typo
        .order-num-inner
          .order1.active 01.
          .order2 02.
          .order3 10.
          .order4 100.
          .order5 ex.
      .content
        .step.step1( v-scroll="step1" )
          | test
        .step.step2( v-scroll="step2" )
          | test
        .step.step10( v-scroll="step10" )
          | test
        .step.step100( v-scroll="step100" )
          | test
        .step.step-ex1( v-scroll="stepEx" )
          | test
        .step.step-ex1
          | test
</template>
<i18n>
  {
    "ja": {},
    "en": {}
  }
</i18n>


<style lang="stylus" scoped>
.order-num
  position sticky
  top 200px
  align-self flex-start
  flex 0 0 auto
  width 20%
  height 80px
  line-height 80px
  color $primary
  font-size 80px
  overflow hidden
  @media (max-width: 1500px)
    width 30%
  @media (max-width: 1050px)
    font-size 60px
  @media (max-width: 750px)
    font-size 34px
    letter-spacing -.1rem
  .order-num-inner
    transition transform .3s ease
  &.step2
    .order-num-inner
      transform translate3d(0, -80px, 0)
  &.step10
    .order-num-inner
      transform translate3d(0, -160px, 0)
  &.step100
    .order-num-inner
      transform translate3d(0, -240px, 0)
  &.step-ex
    .order-num-inner
      transform translate3d(0, -320px, 0)
</style>

<script>
export default {
   methods: {
    step1: function(evt, el) {
      var pos, stepNum;
      stepNum = document.querySelector('.order-num');
      pos = el.getBoundingClientRect().top + window.pageYOffset;
      pos = pos - 250;
      if (window.scrollY > pos) {
        return stepNum.classList.add('step1');
      } else if (window.scrollY < pos) {
        return stepNum.classList.remove('step1');
      }
    },
    step2: function(evt, el) {
      var pos, stepNum;
      stepNum = document.querySelector('.order-num');
      pos = el.getBoundingClientRect().top + window.pageYOffset;
      pos = pos - 250;
      if (window.scrollY > pos) {
        return stepNum.classList.add('step2');
      } else if (window.scrollY < pos) {
        return stepNum.classList.remove('step2');
      }
    },
    step10: function(evt, el) {
      var pos, stepNum;
      stepNum = document.querySelector('.order-num');
      pos = el.getBoundingClientRect().top + window.pageYOffset;
      pos = pos - 250;
      if (window.scrollY > pos) {
        return stepNum.classList.add('step10');
      } else if (window.scrollY < pos) {
        return stepNum.classList.remove('step10');
      }
    },
    step100: function(evt, el) {
      var pos, stepNum;
      stepNum = document.querySelector('.order-num');
      pos = el.getBoundingClientRect().top + window.pageYOffset;
      pos = pos - 250;
      if (window.scrollY > pos) {
        return stepNum.classList.add('step100');
      } else if (window.scrollY < pos) {
        return stepNum.classList.remove('step100');
      }
    },
    stepEx: function(evt, el) {
      var pos, stepNum;
      stepNum = document.querySelector('.order-num');
      pos = el.getBoundingClientRect().top + window.pageYOffset;
      pos = pos - 250;
      if (window.scrollY > pos) {
        return stepNum.classList.add('step-ex');
      } else if (window.scrollY < pos) {
        return stepNum.classList.remove('step-ex');
      }
    }
  }
}
</script>
