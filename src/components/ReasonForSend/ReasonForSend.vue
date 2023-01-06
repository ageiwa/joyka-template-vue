<script setup>
    import { ref } from 'vue'
    import { Swiper, SwiperSlide } from 'swiper/vue'
    import { Navigation, Pagination } from 'swiper'
    import 'swiper/scss'
    import './style.scss'

    const slides = ref([
        {img: 'src/assets/slider-img1.png', title: 'Удивить родных', subtitle: 'Встретились со знаменитостью? Веселитесь на концерте любимой группы? Отдыхаете на экзотическом пляже? Такие фото обязательно должны быть в семейном альбоме!'},
        {img: 'src/assets/slider-img2.png', title: 'Пригласить друзей на вечеринку', subtitle: 'От приглашения, переданного лично в руки,</span> настрой хорошо повеселиться обеспечен'},
        {img: 'src/assets/slider-img3.png', title: 'Прислать привет из путешествия', subtitle: 'В любой точке мира — вы рядом со своими близкими.'},
        {img: 'src/assets/slider-img4.png', title: 'Подарить радость просто так!', subtitle: 'Наша жизнь наполнена рутиной. Отправленная JoyKa с тёплыми словами подарит вашим близким хорошее настроение и улыбку на весь день.'},
        {img: 'src/assets/slider-img5.png', title: 'Поделиться воспоминаниями', subtitle: 'Фотография с фразой: «Помнишь, как классно было?» вызовет волну положительных эмоций и желание встретиться снова.'},
        {img: 'src/assets/slider-img6.png', title: 'Передать привет родителям', subtitle: 'Ваше счастливое фото порадует их больше любого звонка и напомнит им о ваших чувствах.'},
        {img: 'src/assets/slider-img7.png', title: 'Поздравить с праздником', subtitle: 'Удивить друзей, порадовать родных — какая идея может быть лучше для праздника, чем JoyKa?'},
        {img: 'src/assets/slider-img8.png', title: 'Вдохновить близких своими победами', subtitle: 'Забил решающий гол? Покорил очередкую вершину? Отправь JoyKa — пусть друзья разделят с тобой радость момента.'}
    ])

    const navigation = {
        nextEl: '.swiper-button-next',
        prevEl: '.swiper-button-prev'
    }

    const pagination = {
        el: '.swiper-pagination',
        type: 'custom',
        renderCustom: (index, current, total) => {
            if (current < 10) current = '0' + current
            if (total < 10) total = '0' + total

            const curElem = '<span style="font-weight: 700; font-size: 24px; color: #2783FE;">'+current+'</span>'
            const totalElem = '<span class="swiper-pagination-current">'+total+'</span>'

            return curElem + ' / ' + totalElem
        }
    }
    
</script>

<template>
    <div class="reason-for-send">
        <div class="reason-for-send__clouds"></div>

        <div class="container">
            <h1 class="reason-for-send__header-title">Поводы для отправки</h1>

            <swiper :slides-per-view="1" :space-between="-700" :modules="[Navigation, Pagination]" :navigation="navigation" :pagination="pagination">
                
                <SwiperSlide v-for="slide in slides">
                    <div class="slider__item-slider">
                        <div class="item-slider__img-wrap">
                            <img :src="slide.img">
                        </div>
                        <div class="item-slider__text">
                            <h2 class="item-slider__title">{{ slide.title }}</h2>
                            <p class="item-slider__subtitle">{{ slide.subtitle }}</p>
                        </div>
                    </div>
                </SwiperSlide>

                <div class="swiper__control-container">
                    <div class="control-container__navigation">
                        <div class="swiper-button-prev">
                            <div class="swiper__arrow-prev"></div>
                        </div>

                        <div class="swiper-button-next">
                            <div class="swiper__arrow-next"></div>
                        </div>
                    </div>

                    <p class="control-panel__text">Листайте дальше</p>

                    <div class="swiper-pagination"></div>
                </div>
                
            </swiper>

        </div>
        <div class="reason-for-send__wave"></div>
    </div>
</template>