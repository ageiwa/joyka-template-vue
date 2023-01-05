<script setup>
    import { ref } from 'vue'
    import SendJoykaBtn from '@/components/SendJoykaBtn/SendJoykaBtn.vue'

    const countries = ref([
        {id: 'country1', name: 'Украина', img: '/src/assets/country1.png'},
        {id: 'country2', name: 'Грузия', img: '/src/assets/country2.png'},
        {id: 'country3', name: 'Тайланд', img: '/src/assets/country3.png'},
        {id: 'other-country', name: 'Еще страна', img: '/src/assets/empty-country.png'}
    ])

    const currentStep = ref(1)
    const totalStep = ref(4)
    const progressLine = ref(calcProgress())

    function prevStep() {
        if (currentStep.value > 1) currentStep.value--
        progressLine.value = calcProgress()
    }

    function nextStep() {
        if (currentStep.value < totalStep.value) currentStep.value++
        progressLine.value = calcProgress()
    }

    function calcProgress() {
        return (currentStep.value / totalStep.value) * 100
    }

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
                        <p class="progress__step">Шаг {{ currentStep }} из {{ totalStep }}</p>
                        <div class="progress__progress-wrap">
                            <div :style="{width: progressLine + '%'}" class="progress__progress-line"></div>
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
                        <SendJoykaBtn :title="'Предыдущий шаг'" @click="prevStep" />
                        <SendJoykaBtn :title="'Следующий шаг'" @click="nextStep" />
                    </div>
                </div>
            </form>

        </div>
    </div>
</template>

<style scoped lang="scss">
    @import './style.scss'
</style>