<script setup>

</script>
    
<template>
    <div class="header__select-lang">
        <span class="select-lang__title">EN</span>
        <img class="select-lang__flag-icon" src="@/assets/us.png">
        <img class="select-lang__arrow-icon" src="@/assets/arrow.png">

        <ul class="select-lang__lang-list">
            <div class="lang-list__arrow"></div>
            <li class="lang-list__item">
                <span class="lang-list__title">EN</span>
                <img class="select-lang__flag-icon" src="@/assets/us.png">
            </li>
            <li class="lang-list__item">
                <span class="lang-list__title">RU</span>
                <img class="select-lang__flag-icon" src="@/assets/russia.png">
            </li>
        </ul>
    </div>
</template>

<style scoped lang="scss">
  @import './style.scss'
</style>
