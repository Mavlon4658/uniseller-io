<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue';

// Import Swiper styles
import 'swiper/css';

import 'swiper/css/pagination';
import 'swiper/css/navigation';

// import required modules
import { Autoplay, Pagination, Navigation } from 'swiper/modules';
export default {
    name: 'Home',
    components: {
        Swiper,
        SwiperSlide,
    },
    setup() {
        return {
            modules: [Autoplay, Pagination, Navigation],
        };
    },
    methods: {
        getUrl (name) {
            return new URL(name, import.meta.url).href;
        }
    }
}
</script>

<template>
    <!-- Home -->
    <section class="home">
        <div class="main_container home__container">
            <div class="home__left">
                <img src="@/assets/images/logo-xl.svg" alt="">
                <h2>uniseller<span>.</span>io</h2>
                <p>автоматизация бизнеса на маркетплейсах</p>
            </div>
            <div class="home__right">
                <h3>Все необходимое <br>для селлеров <br> <span>Маркетплейсов</span></h3>
                <p>Уникальный инструмент, способный объеденить в одном окне упаравление продажами  на всех доступных маркетплейсах. Добавляйте организации, подключайте каналы продаж, создавайте карточки товаров, добавляйте ассортимент, контролируйте цены,  заказы и отгрузки. <br> С помощью Uniseller вы сможете масштабировать продажи и работать <br>с любым количеством личных кабинетов. Получите возможность подключения к “1С” , “Мой Склад” либо с другим вашим сервисом.</p>
                <a href="#" class="btn_yellow">
                    <span>Подробнее о UniSeller</span>
                    <img src="@/assets/images/youtube.svg" alt="">
                </a>
            </div>
        </div>
    </section>
    <!-- Home end -->

    <!-- Partners -->
    <section class="partners">
        <swiper
            :slidesPerView="'auto'"
            :spaceBetween="53"
            :autoplay="{
                delay: 2500,
                disableOnInteraction: false,
            }"
            :modules="modules"
            class="mySwiper"
        >
            <swiper-slide v-for="i in 5" :key="i">
                <img :src="require('@/assets/images/partner-1-'+i+'.png')" alt="">
            </swiper-slide>
        </swiper>
    </section>
    <!-- Partners end -->
</template>

<style>

</style>