<script setup>
    import { ref } from 'vue'
    import SendJoykaBtn from '@/components/SendJoykaBtn/SendJoykaBtn.vue'
    import './style.scss'
    import './media.scss'

    const data = ref([
        {
            step: 1,
            title: 'Выберите страну отправления',
            data: [
                {id: 'country1', name: 'Украина', img: '/src/assets/country1.png', checked: false},
                {id: 'country2', name: 'Грузия', img: '/src/assets/country2.png', checked: false},
                {id: 'country3', name: 'Тайланд', img: '/src/assets/country3.png', checked: false},
                {id: 'other-country', name: 'Еще страна', img: '/src/assets/other.png', checked: false}
            ]
        },
        {
            step: 2,
            title: 'Выберите время отправления',
            data: [
                {id: 'time1', name: 'Утром', img: '/src/assets/time1.png', checked: false},
                {id: 'time2', name: 'Днем', img: '/src/assets/time2.png', checked: false},
                {id: 'time3', name: 'Вечером', img: '/src/assets/time3.png', checked: false},
                {id: 'other-time', name: 'Другое время', img: '/src/assets/other.png', checked: false}
            ]
        },
        {
            step: 3,
            title: 'Выберите социальную сеть для доставки',
            data: [
                {id: 'soc1', name: 'VK', img: '/src/assets/soc1.png', checked: false},
                {id: 'soc2', name: 'Одноклассники', img: '/src/assets/soc2.png', checked: false},
                {id: 'soc3', name: 'E-Mail', img: '/src/assets/soc3.png', checked: false},
                {id: 'other-soc', name: 'Другой способ', img: '/src/assets/other.png', checked: false}
            ]
        },
        {
            step: 4,
            title: 'Выберите голос озвучивания Joyka',
            data: [
                {id: 'voice1', name: 'Виктор', img: '/src/assets/voice1.png', checked: false},
                {id: 'voice2', name: 'Елена', img: '/src/assets/voice2.png', checked: false},
                {id: 'voice3', name: 'Максим', img: '/src/assets/voice3.png', checked: false},
                {id: 'other-voice', name: 'Выбрать свой', img: '/src/assets/other.png', checked: false}
            ]
        },
    ])

    const stepTitle = ref('')
    const stepData = ref([])

    const currentStep = ref(1)
    const totalStep = ref(4)

    const progressLineMobile = ref(0)
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
        const step = data.value[currentStep.value - 1]
        const progressPrecent = (currentStep.value / totalStep.value) * 100

        stepTitle.value = step.title
        stepData.value = step.data

        const c = Math.PI * (45 * 2)
        const pct = ((100 - progressPrecent) / 100) * c

        progressLineMobile.value = pct

        return progressPrecent
    }

    function handleCheck(e) {
        data.value.forEach(item => {
            if (item.step === currentStep.value) {
                item.data.forEach(value => {
                    if (value.checked && value.id !== e.target.id) value.checked = false
                })

                const obj = item.data.find(input => input.id === e.target.id)
                obj.checked = !obj.checked
                
            }
        })
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

                    <div class="choice__header">
                        <div class="choice__progress">
                            <p class="progress__step">Шаг {{ currentStep }} из {{ totalStep }}</p>
                            <div class="progress__progress-wrap">
                                <div :style="{width: progressLine + '%'}" class="progress__progress-line"></div>
                            </div>
                        </div>

                        <div class="choice__progress-mobile">
                            <svg class="progress-line-mobile" id="svg" width="90" height="90" viewPort="0 0 100 100" version="1.1" xmlns="http://www.w3.org/2000/svg">
                                <circle cx="45" cy="45" r="45" :style="{strokeDashoffset: progressLineMobile, strokeWidth: 20, strokeDasharray: 283}" transform-origin="center" transform="rotate(-90)" fill="rgba(0,0,0,0)" stroke="#2783FE"></circle>
                            </svg>
                            <!-- <div class="progress-line-mobile"></div> -->
                            <div class="progress-mobile__title">
                                {{ currentStep }} из {{ totalStep }}
                            </div>
                        </div>

                        <h2 class="select-country__title">{{ stepTitle }}</h2>
                    </div>

                    <div class="select-country__county-wrap">
                        <div v-for="data in stepData" class="country-wrap__country">
                            <label :for="data.id" class="country__label">
                                <div class="label__img-wrap">
                                    <img :src="data.img">
                                </div>
                                {{ data.name }}
                            </label>
                            <input @click="handleCheck" class="country__input" :id="data.id" type="radio" name="country" :checked="data.checked">
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