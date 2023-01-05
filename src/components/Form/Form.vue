<script setup>
    import { ref } from 'vue'
    import SendJoykaBtn from '@/components/SendJoykaBtn/SendJoykaBtn.vue'

    const countries = ref([
        {id: 'country1', name: 'Украина', img: '/src/assets/country1.png'},
        {id: 'country2', name: 'Грузия', img: '/src/assets/country2.png'},
        {id: 'country3', name: 'Тайланд', img: '/src/assets/country3.png'},
        {id: 'other-country', name: 'Еще страна', img: '/src/assets/empty-country.png'}
    ])
</script>

<template>
    <div class="order-form">
        <div class="container">

            <form class="form">
                <div class="form__img-wrap">
                    <img src="@/assets/girl-form.png">
                </div>
                <div class="form__choice">

                    <div class="choice__progress">
                        <p class="progress__step">Шаг 1 из 5</p>
                        <div class="progress__progress-wrap">
                            <div class="progress__progress-line"></div>
                        </div>
                    </div>

                    <div class="choice__select-country">
                        <h2 class="select-country__title">Выберите страну отправления</h2>

                        <div class="select-country__county-wrap">

                            <div v-for="country in countries" class="country-wrap__country">
                                <label :for="country.id" class="country__label">
                                    <div class="label__img-wrap">
                                        <img :src="country.img">
                                    </div>
                                    {{ country.name }}
                                </label>
                                <input class="country__input" :id="country.id" type="radio" name="country">
                            </div>

                        </div>
                    </div>

                    <div class="choice__btns-wrap">
                        <SendJoykaBtn :title="'Предыдущий шаг'" />
                        <SendJoykaBtn :title="'Следующий шаг'" />
                    </div>
                </div>
            </form>

        </div>
    </div>
</template>

<style scoped lang="scss">
    @import './style.scss'
</style>