<script setup>
  import SelectLanguage from '@/components/SelectLanguage/SelectLanguage.vue'
  import './style.scss'
  import './media.scss'
  import { ref } from 'vue';

  const showMobileMenu = ref(false)

  function openMenu() {
    showMobileMenu.value = !showMobileMenu.value
  }
</script>

<template>
  <header class="header">
    <div class="container">

      <div class="header__logo">
        <a href="#">
          <img src="@/assets/logo.png">
        </a>
      </div>

      <nav class="header__navbar">
        <ul>
          <li class="navbar__item"><a href="#">Как это работает?</a></li>
          <li class="navbar__item"><a href="#">Кто мы?</a></li>
          <li class="navbar__item"><a href="#">Поводы для отправки</a></li>
          <li class="navbar__item"><a href="#">FAQ</a></li>
          <li class="navbar__item"><a href="#">Отзывы</a></li>
        </ul>
      </nav>

      <SelectLanguage />

      <div class="burger-menu-wrap">
        <div @click="openMenu" :class="{'burger-menu': true, 'burger-menu_active': showMobileMenu}">
          <div class="burger-menu__line"></div>
          <div class="burger-menu__line"></div>
          <div class="burger-menu__line"></div>
        </div>
      </div>

      <nav :class="{'header__navbar-mobile': true, 'header__navbar-mobile_active': showMobileMenu}">
          <ul>
            <li class="navbar-mobile__item"><a href="#">Как это работает?</a></li>
            <li class="navbar-mobile__item"><a href="#">Кто мы?</a></li>
            <li class="navbar-mobile__item"><a href="#">Поводы для отправки</a></li>
            <li class="navbar-mobile__item"><a href="#">FAQ</a></li>
            <li class="navbar-mobile__item"><a href="#">Отзывы</a></li>
          </ul>
        </nav>

    </div>
  </header>
</template>
