<script setup>
    import SendJoykaBtn from '@/components/SendJoykaBtn/SendJoykaBtn.vue'
    import './style.scss'
</script>

<template>
    <div class="how-it-works">
        <div class="container">

            <h1 class="how-it-works__header-title">Как это работает?</h1>

            <ul class="how-it-works__step-list">

                <li class="step-list__item-step">
                    <div class="item-step__wrap-img">
                        <img class="item-step__img" src="@/assets/girl-selfie.png">
                    </div>
                    <div class="item-step__dots-wrap">
                        <div class="item-step__dots"></div>
                        <div class="item-step__dots"></div>
                        <div class="item-step__dots"></div>
                    </div>
                    <div class="item-step__text">
                        <h2 class="item-step__title">Человек делает селфи</h2>
                        <p class="item-step__subtitle">Вы делаете селфи или выбираете удачное фото из галереи JoyKa</p>
                    </div>
                    <p class="item-step__step">1</p>
                </li>

                <li class="step-list__item-step">
                    <div class="item-step__wrap-img">
                        <img class="item-step__img" src="@/assets/girl-phone.png">
                    </div>
                    <div class="item-step__dots-wrap">
                        <div class="item-step__dots"></div>
                        <div class="item-step__dots"></div>
                        <div class="item-step__dots"></div>
                    </div>
                    <div class="item-step__text">
                        <h2 class="item-step__title">Конверт JoyKa с ярким фото</h2>
                        <p class="item-step__subtitle">Оставляете заявку на сайте или в приложении. Две минуты — и JoyKa готова!</p>
                    </div>
                    <p class="item-step__step">2</p>
                </li>

                <li class="step-list__item-step">
                    <div class="item-step__wrap-img">
                        <img class="item-step__img" src="@/assets/man-chocolate.png">
                    </div>
                    <div class="item-step__dots-wrap last-dots">
                        <div class="item-step__dots"></div>
                        <div class="item-step__dots"></div>
                        <div class="item-step__dots"></div>
                    </div>
                    <div class="item-step__text">
                        <h2 class="item-step__title">Курьер несёт JoyKa</h2>
                        <p class="item-step__subtitle">Распечатанную фотографию в красивом конверте курьер доставит лично в руки адресату</p>
                    </div>
                    <p class="item-step__step">3</p>
                </li>

                <li class="step-list__item-step step-address">
                    <div class="item-step__wrap-img">
                        <img class="item-step__img" src="@/assets/love-voxel.png">
                        <img class="item-step__img" src="@/assets/girl-address.png">
                    </div>
                    <div class="item-step__text">
                        <h2 class="item-step__title">Адресат радуется полученной JoyKa</h2>
                        <p class="item-step__subtitle">Ваше фото с личным посланием подарят близким хорошее настроение на весь день</p>
                        <SendJoykaBtn :title="'Отправить Джойку'" :showIcon="true" />
                    </div>
                    <p class="item-step__step">4</p>
                </li>

            </ul>

        </div>
    </div>
</template>