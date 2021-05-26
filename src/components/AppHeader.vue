<template>
  <header class="header">
    <div class="overlay has-fade"></div>
    <nav class="container container--p-all flex flex-jc-sb flex-ai-c">
        <a href="/" class="header__logo">
          <img src="../assets/images/logo.svg" alt="Easybank" />
        </a>

        <a href="#" class="header__toggle hide-for-desktop sr-only" @click="openMenu">
          <span></span>
          <span></span>
          <span></span>
          Text
        </a>

        <div class="header__links hide-for-mobile">
          <a href="#">Home</a>
          <a href="#">About</a>
          <a href="#">Contact</a>
          <a href="#">Blog</a>
          <a href="#">Careers</a>
        </div>

        <button type="button" class="hide-for-mobile">Request Invite</button>
    </nav>
    <div class="header__menu has-fade">
      <a href="">Home</a>
      <a href="">About</a>
      <a href="">Contact</a>
      <a href="">Blog</a>
      <a href="">Careers</a>
    </div>
  </header>
</template>

<script>
export default {
  name: 'AppHeader',
  setup () {
    function openMenu () {
      const header = document.querySelector('.header')
      const fadeElems = document.querySelectorAll('.has-fade')
      const body = document.querySelector('body')
      if (header.classList.contains('open')) {
        body.classList.remove('noscroll')
        header.classList.remove('open')
        fadeElems.forEach(function (element) {
          element.classList.remove('fade-in')
          element.classList.add('fade-out')
        })
      } else {
        body.classList.add('noscroll')
        header.classList.add('open')
        fadeElems.forEach(function (element) {
          element.classList.remove('fade-out')
          element.classList.add('fade-in')
        })
      }
    }
    return {
      openMenu
    }
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/scss/sections/header.scss'
</style>
