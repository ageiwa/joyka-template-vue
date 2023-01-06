<script setup>
    import { ref } from 'vue'
    import './style.scss'

    const lang = ref('EN')
    const langIcon = ref('/src/assets/us.png')
    
    const languages = ref([
        {id: 1, name: 'EN', icon: '/src/assets/us.png'},
        {id: 2, name: 'RU', icon: '/src/assets/russia.png'},
    ])

    function selectLang(id) {
        lang.value = languages.value.find(lang => lang.id === id).name
        langIcon.value = languages.value.find(lang => lang.id === id).icon
    }
</script>
    
<template>
    <div class="header__select-lang">

        <span class="select-lang__title">{{ lang }}</span>
        <img class="select-lang__flag-icon" :src="langIcon">
        <img class="select-lang__arrow-icon" src="@/assets/arrow.png">

        <ul class="select-lang__lang-list">
            <div class="lang-list__arrow"></div>

            <li v-for="lang in languages" :id="lang.id" class="lang-list__item" @click="selectLang(lang.id)">
                <span class="lang-list__title">{{ lang.name }}</span>
                <img class="select-lang__flag-icon" :src="lang.icon">
            </li>
        </ul>

    </div>
</template>
