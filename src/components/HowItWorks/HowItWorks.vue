<script setup>
    import SendJoykaBtn from '@/components/SendJoykaBtn/SendJoykaBtn.vue';
</script>

<template>
    <div class="how-it-works">
        <div class="container">

            <h1 class="how-it-works__header-title">Как это работает?</h1>

            <ul class="how-it-works__list-steps">

                <div class="list-steps__container">

                    <li class="list-steps__item-steps">
                        <div class="item-steps__wrap-img">
                            <img class="item-steps__img" src="@/assets/girl-selfie.png">
                        </div>
                        <div class="item-steps__text">
                            <img class="item-steps__step-number" src="@/assets/1.png">
                            <h2 class="item-steps__title">Человек<br>делает селфи</h2>
                            <p class="item-steps__subtitle">Вы делаете селфи<br>или выбираете удачное фото<br>из галереи JoyKa</p>
                        </div>
                    </li>
                    
                    <li class="list-steps__item-steps">
                        <div class="item-steps__wrap-img">
                            <img class="item-steps__img" src="@/assets/girl-phone.png">
                        </div>
                        <div class="item-steps__text">
                            <img class="item-steps__step-number" src="@/assets/2.png">
                            <h2 class="item-steps__title">Конверт<br>JoyKa с ярким фото</h2>
                            <p class="item-steps__subtitle">Оставляете заявку на сайте<br>или в приложении. Две минуты<br> — и JoyKa готова!</p>
                        </div>
                    </li>

                    <li class="list-steps__item-steps">
                        <div class="item-steps__wrap-img">
                            <img class="item-steps__img" src="@/assets/man-chocolate.png">
                        </div>
                        <div class="item-steps__text">
                            <img class="item-steps__step-number" src="@/assets/3.png">
                            <h2 class="item-steps__title">Курьер несёт<br>JoyKa</h2>
                            <p class="item-steps__subtitle">Распечатанную фотографию<br>в красивом конверте курьер<br>доставит лично в руки адресату</p>
                        </div>
                    </li>

                </div>

                <li class="list-steps__item-steps address-step">
                    <div class="item-steps__rect-steps">
                        <img class="rect-steps__img" src="@/assets/love-voxel.png">
                        <img class="rect-steps__img" src="@/assets/girl-address.png">
                    </div>

                    <div class="item-steps__text">
                        <div class="address-step-text">
                            <img class="item-steps__step-number" src="@/assets/4.png">
                            <h2 class="item-steps__title">Адресат радуется полученной JoyKa</h2>
                            <p class="item-steps__subtitle">Ваше фото с личным посланием подарят<br>близким хорошее настроение на весь день</p>
                        </div>

                        <SendJoykaBtn />
                    </div>

                </li>
            </ul>

        </div>
    </div>
</template>

<style scoped lang="scss">
    @import './style.scss'
</style>