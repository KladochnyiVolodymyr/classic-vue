<template>
  <div>
    <app-header/>
    <transition name="fade">
      <nuxt/>
    </transition>
    <app-footer/>
  </div>
</template>
<script>
import AppHeader from '~/components/AppHeader.vue'
import AppFooter from '~/components/AppFooter.vue'
export default {
  components: {
    AppHeader,
    AppFooter
  }
}
</script>

<style lang="sass">
@import '~assets/reset'
.container
  width: 940px
  margin: 0 auto
.wrapper
  min-height: calc(100vh - 150px)
.fade-enter-active, .fade-leave-active 
  transition: opacity .7s
.fade-enter, .fade-leave-to 
  opacity: 0
</style>
