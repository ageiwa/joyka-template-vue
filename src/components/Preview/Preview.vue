<script setup>
    import SendJoykaBtn from '@/components/SendJoykaBtn/SendJoykaBtn.vue'
</script>

<template>
    <div class="preview">
        
        <div class="container">
            <h1 class="preview__title">JoyKa — эмоции в конверте<br>Дари моменты радости<br>вместе с JoyMail!</h1>
            
            <ul class="preview__list-preview">
                <li class="list-preview__item-preview">
                    <img class="item-preview__icon" src="@/assets/icon-list.png">
                    Доставка из любой точки мира
                </li>
                <li class="list-preview__item-preview">
                    <img class="item-preview__icon" src="@/assets/icon-list.png">
                    За 12 часов
                </li>
                <li class="list-preview__item-preview">
                    <img class="item-preview__icon" src="@/assets/icon-list.png">
                    Лично в руки адресату
                </li>
            </ul>

            <div class="preview__btns-preview">

                <SendJoykaBtn />

                <div class="btns-preview__btn-play-wrap">
                    <div class="btns-preview__btn-play">
                        <img class="btn-play-wrap__btn-play-icon" src="@/assets/preview-btn-play.png">
                    </div>
                    <div class="btn-play-wrap__title">
                        <p>Посмотрите видеообзор<br>нашего подарка</p>
                        <span>Время просмотра 1:23 сек</span>
                    </div>
                </div>

            </div>

        </div>

        <div class="preview__clouds"></div>
    </div>
</template>

<style scoped lang="scss">
    @import './style.scss'
</style>