<script setup>
    import SendJoykaBtn from '@/components/SendJoykaBtn/SendJoykaBtn.vue'
</script>

<template>
    <div class="preview">
        
        <div class="container">
            <h1 class="preview__title">JoyKa — эмоции в конверте Дари моменты радости вместе с JoyMail!</h1>
            
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

                <div class="btn-play-container">
                    <div class="btn-play">
                        <svg width="74" height="73" viewBox="0 0 74 73" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <g filter="url(#filter0_i_23_187)">
                            <path d="M37.0037 73C16.5764 72.9779 0.022433 56.6492 0 36.5V35.77C0.406787 15.7116 17.1497 -0.262894 37.4872 0.00327849C57.8248 0.269451 74.1321 16.6765 73.9992 36.7385C73.8663 56.8005 57.343 72.996 37.0037 73ZM32.7924 22.4346C31.4723 21.458 29.603 22.4004 29.603 24.0424V48.9576C29.603 50.5997 31.4723 51.5421 32.7924 50.5655L49.6318 38.1079C50.7125 37.3084 50.7125 35.6917 49.6318 34.8922L32.7924 22.4346Z" fill="url(#paint0_linear_23_187)" />
                            </g>
                            <defs>
                            <filter id="filter0_i_23_187" x="0" y="0" width="74" height="73" filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB">
                            <feFlood flood-opacity="0" result="BackgroundImageFix"/>
                            <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape"/>
                            <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha"/>
                            <feOffset/>
                            <feGaussianBlur stdDeviation="2.5"/>
                            <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1"/>
                            <feColorMatrix type="matrix" values="0 0 0 0 1 0 0 0 0 1 0 0 0 0 1 0 0 0 0.25 0"/>
                            <feBlend mode="normal" in2="shape" result="effect1_innerShadow_23_187"/>
                            </filter>
                            <linearGradient id="paint0_linear_23_187" x1="38.9637" y1="-2.76125e-07" x2="45.4406" y2="72.4207" gradientUnits="userSpaceOnUse">
                            <stop stop-color="#7BC0FF"/>
                            <stop offset="1" stop-color="#2783FE"/>
                            </linearGradient>

                            <linearGradient id="hover-gradient" x1="38.9637" y1="-2.76125e-07" x2="45.4406" y2="72.4207" gradientUnits="userSpaceOnUse">
                            <stop stop-color="#C1E1FF"/>
                            <stop offset="1" stop-color="#4595FF"/>
                            </linearGradient>
                            </defs>
                        </svg>
                    </div>
                    
                    <div class="btn-play-container__text">
                        <p>Посмотрите видеообзор нашего подарка</p>
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