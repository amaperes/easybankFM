<template>
  <app-header/>
  <app-hero />
  <app-features />
  <app-articles />
  <app-footer/>
  <div class="attribution">
    Challenge by <a href="https://www.frontendmentor.io?ref=challenge" target="_blank">Frontend Mentor</a>
    Coded by <a href="https://github.com/amaperes">A.P.</a>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue'
import AppHero from './components/main/AppHero.vue'
import AppFeatures from './components/main/AppFeatures.vue'
import AppArticles from './components/main/AppArticles.vue'
import AppFooter from './components/AppFooter.vue'

export default {
  name: 'App',
  components: {
    AppHeader,
    AppHero,
    AppFeatures,
    AppArticles,
    AppFooter
  }
}
</script>

<style lang="scss">
@import "./assets/scss/style.scss";
  .attribution { font-size: 11px; text-align: center; }
  .attribution a { color: hsl(228, 45%, 44%); }
</style>
