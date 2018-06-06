<template>
  <div>
    <app-header/>
    <nuxt/>
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

</style>
