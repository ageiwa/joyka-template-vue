<script setup>
    import './style.scss'
</script>

<template>
    <footer class="footer">
        <div class="container">
            <div class="footer__wrap">

                <a href="#" class="footer__logo-wrap">
                    <img src="@/assets/logo-footer.png">
                    <p class="footer__logo-text">Радовать людей — это наша работа</p>
                </a>

                <ul class="footer__list-link">
                    <li class="list-link__item-link">
                        <a href="#">Политика безопасности</a>
                    </li>
                    <li  class="list-link__item-link">
                        <a href="#">Контакты</a>
                    </li>
                    <li  class="list-link__item-link">
                        <a href="#">Партнерам</a>
                    </li>
                </ul>

                <div class="footer__pays">
                    <a href="#" class="pays__link-pay">
                        <img src="@/assets/LIQPAY 1.png">
                    </a>
                    <a href="#" class="pays__link-pay">
                        <img src="@/assets/visa.png">
                    </a>
                    <a href="#" class="pays__link-pay">
                        <img src="@/assets/master card.png">
                    </a>
                </div>

            </div>
            <div class="footer__wrap">
                <ul class="footer__social-list">
                    <li class="footer__social-link">
                        <a href="#">
                            <img src="@/assets/instagramm.png">
                        </a>
                    </li>
                    <li class="footer__social-link">
                        <a href="#">
                            <img src="@/assets/facebook.png">
                        </a>
                    </li>
                    <li class="footer__social-link">
                        <a href="#">
                            <img src="@/assets/telegramm.png">
                        </a>
                    </li>
                    <li class="footer__social-link">
                        <a href="#">
                            <img src="@/assets/youtube.png">
                        </a>
                    </li>
                </ul>
                <p class="footer__copyright">Дизайн сайта - Алесей Киселев</p>
            </div>

        </div>
    </footer>
</template>