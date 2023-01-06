<script setup>
  import SelectLanguage from '@/components/SelectLanguage/SelectLanguage.vue'
  import './style.scss'
  import './media.scss'
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

    </div>
  </header>
</template>
