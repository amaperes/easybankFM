<template>
  <app-header/>
  <app-hero />
</template>

<script>
import AppHeader from './components/AppHeader.vue'
import AppHero from './components/main/AppHero.vue'

export default {
  name: 'App',
  components: {
    AppHeader,
    AppHero
  }
}
</script>

<style lang="scss">
@import "./assets/scss/style.scss";
</style>
