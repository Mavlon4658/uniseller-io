<script>
export default {
    name: 'Header',
    data () {
        return {
            accordion: null,
            menu: false
        }
    },
    watch: {
        menu () {
            if (this.menu) {
                document.querySelector('body').style.overflow = 'hidden';
            } else {
                document.querySelector('body').style.overflow = 'visible';
            }
        }
    },
    methods: {
        toggleAccordion (data) {
            this.accordion = this.accordion == data ? null : data
        }
    }
}
</script>

<template>
    <header class="header">
        <div class="main_container header__container">
            <div class="header__left">
                <a href="/" class="header__logo">
                    <img src="@/assets/images/logo.svg" alt="">
                    <span class="header__logo_text">uniseller<span>.</span>io</span>
                </a>
                <ul class="header__nav">
                    <li class="header__nav_item">
                        <a href="#" class="header__nav_link">
                            <span>Услуги</span>
                            <svg width="9" height="5" viewBox="0 0 9 5" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M0.883789 1L4.38379 4L7.88379 0.999999" stroke="#EF6C1E" stroke-linecap="round" stroke-linejoin="round"/>
                            </svg>
                        </a>
                        <ul class="header__nav_list">
                            <li>
                                <a href="#">Личные кабинеты</a>
                            </li>
                            <li>
                                <a href="#">Цены и остатки</a>
                            </li>
                            <li>
                                <a href="#">Ассортимент</a>
                            </li>
                            <li>
                                <a href="#">Подключение</a>
                            </li>
                            <li>
                                <a href="#">Аналитика</a>
                            </li>
                        </ul>
                    </li>
                    <li class="header__nav_item">
                        <a href="#" class="header__nav_link">
                            <span>Интеграции</span>
                            <svg width="9" height="5" viewBox="0 0 9 5" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M0.883789 1L4.38379 4L7.88379 0.999999" stroke="#EF6C1E" stroke-linecap="round" stroke-linejoin="round"/>
                            </svg>
                        </a>
                        <ul class="header__nav_list">
                            <li>
                                <a href="#">1С</a>
                            </li>
                            <li>
                                <a href="#">Мой склад</a>
                            </li>
                            <li>
                                <a href="#">API</a>
                            </li>
                            <li>
                                <a href="#">Решения</a>
                            </li>
                            <li>
                                <a href="#">Сторонние сервисы</a>
                            </li>
                        </ul>
                    </li>
                    <li class="header__nav_item">
                        <a href="#" class="header__nav_link">
                            <span>Маркетплейсы</span>
                            <svg width="9" height="5" viewBox="0 0 9 5" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M0.883789 1L4.38379 4L7.88379 0.999999" stroke="#EF6C1E" stroke-linecap="round" stroke-linejoin="round"/>
                            </svg>
                        </a>
                        <ul class="header__nav_list">
                            <li>
                                <a href="#">Ozon</a>
                            </li>
                            <li>
                                <a href="#">Яндекс Маркет</a>
                            </li>
                            <li>
                                <a href="#">Мегамаркет</a>
                            </li>
                            <li>
                                <a href="#">Wildberries</a>
                            </li>
                            <li>
                                <a href="#">Avito</a>
                            </li>
                        </ul>
                    </li>
                    <li class="header__nav_item">
                        <a href="#" class="header__nav_link">
                            <span>Тарифы</span>
                            <svg width="9" height="5" viewBox="0 0 9 5" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M0.883789 1L4.38379 4L7.88379 0.999999" stroke="#EF6C1E" stroke-linecap="round" stroke-linejoin="round"/>
                            </svg>
                        </a>
                        <ul class="header__nav_list">
                            <li>
                                <a href="#">Basic</a>
                            </li>
                            <li>
                                <a href="#">Seller</a>
                            </li>
                            <li>
                                <a href="#">SellerPro</a>
                            </li>
                            <li>
                                <a href="#">SellerTop</a>
                            </li>
                            <li>
                                <a href="#">MegaSeller</a>
                            </li>
                        </ul>
                    </li>
                    <li class="header__nav_item">
                        <a href="#" class="header__nav_link">
                            <span>FAQ</span>
                            <svg width="9" height="5" viewBox="0 0 9 5" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M0.883789 1L4.38379 4L7.88379 0.999999" stroke="#EF6C1E" stroke-linecap="round" stroke-linejoin="round"/>
                            </svg>
                        </a>
                        <ul class="header__nav_list">
                            <li>
                                <a href="#">Личные кабинеты</a>
                            </li>
                            <li>
                                <a href="#">Цены и остатки</a>
                            </li>
                            <li>
                                <a href="#">Ассортимент</a>
                            </li>
                            <li>
                                <a href="#">Подключение</a>
                            </li>
                            <li>
                                <a href="#">Аналитика</a>
                            </li>
                        </ul>
                    </li>
                </ul>
            </div>
            <div class="header__right">
                <button class="btn_orange">Оставить заявку</button>
                <ul class="header__auth">
                    <li>
                        <a href="#">Войти</a>
                    </li>
                    <li>
                        <a href="#">Регистрация</a>
                    </li>
                </ul>
                <div class="header__settings">
                    <a href="#">
                        <img src="@/assets/images/user-circle.svg" alt="">
                    </a>
                    <a href="#">
                        <img src="@/assets/images/settings-icon.svg" alt="">
                    </a>
                </div>
                <button class="bars" @click="menu = true">
                    <img src="@/assets/images/bars.svg" alt="">
                </button>
            </div>
        </div>
    </header>

    <div class="mobile_menu" :class="menu ? 'active' : ''">
        <button class="close" @click="menu = false">
            <img src="@/assets/images/times.svg" alt="">
        </button>
        <ul class="mobile_menu__nav">
            <li class="mobile_menu__nav_item">
                <button @click="toggleAccordion('Услуги')">
                    <span>Услуги</span>
                    <svg width="9" height="5" viewBox="0 0 9 5" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M0.883789 1L4.38379 4L7.88379 0.999999" stroke="#EF6C1E" stroke-linecap="round" stroke-linejoin="round"/>
                    </svg>
                </button>
                <ul class="mobile_menu__nav_list" :class="accordion == 'Услуги' ? 'active' : ''">
                    <li>
                        <a href="#">Личные кабинеты</a>
                    </li>
                    <li>
                        <a href="#">Цены и остатки</a>
                    </li>
                    <li>
                        <a href="#">Ассортимент</a>
                    </li>
                    <li>
                        <a href="#">Подключение</a>
                    </li>
                    <li>
                        <a href="#">Аналитика</a>
                    </li>
                </ul>
            </li>
            <li class="mobile_menu__nav_item">
                <button @click="toggleAccordion('Интеграции')">
                    <span>Интеграции</span>
                    <svg width="9" height="5" viewBox="0 0 9 5" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M0.883789 1L4.38379 4L7.88379 0.999999" stroke="#EF6C1E" stroke-linecap="round" stroke-linejoin="round"/>
                    </svg>
                </button>
                <ul class="mobile_menu__nav_list" :class="accordion == 'Интеграции' ? 'active' : ''">
                    <li>
                        <a href="#">1С</a>
                    </li>
                    <li>
                        <a href="#">Мой склад</a>
                    </li>
                    <li>
                        <a href="#">API</a>
                    </li>
                    <li>
                        <a href="#">Решения</a>
                    </li>
                    <li>
                        <a href="#">Сторонние сервисы</a>
                    </li>
                </ul>
            </li>
            <li class="mobile_menu__nav_item">
                <button @click="toggleAccordion('Маркетплейсы')">
                    <span>Маркетплейсы</span>
                    <svg width="9" height="5" viewBox="0 0 9 5" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M0.883789 1L4.38379 4L7.88379 0.999999" stroke="#EF6C1E" stroke-linecap="round" stroke-linejoin="round"/>
                    </svg>
                </button>
                <ul class="mobile_menu__nav_list" :class="accordion == 'Маркетплейсы' ? 'active' : ''">
                    <li>
                        <a href="#">Ozon</a>
                    </li>
                    <li>
                        <a href="#">Яндекс Маркет</a>
                    </li>
                    <li>
                        <a href="#">Мегамаркет</a>
                    </li>
                    <li>
                        <a href="#">Wildberries</a>
                    </li>
                    <li>
                        <a href="#">Avito</a>
                    </li>
                </ul>
            </li>
            <li class="mobile_menu__nav_item">
                <button @click="toggleAccordion('Тарифы')">
                    <span>Тарифы</span>
                    <svg width="9" height="5" viewBox="0 0 9 5" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M0.883789 1L4.38379 4L7.88379 0.999999" stroke="#EF6C1E" stroke-linecap="round" stroke-linejoin="round"/>
                    </svg>
                </button>
                <ul class="mobile_menu__nav_list" :class="accordion == 'Тарифы' ? 'active' : ''">
                    <li>
                        <a href="#">Basic</a>
                    </li>
                    <li>
                        <a href="#">Seller</a>
                    </li>
                    <li>
                        <a href="#">SellerPro</a>
                    </li>
                    <li>
                        <a href="#">SellerTop</a>
                    </li>
                    <li>
                        <a href="#">MegaSeller</a>
                    </li>
                </ul>
            </li>
            <li class="mobile_menu__nav_item">
                <button @click="toggleAccordion('FAQ')">
                    <span>FAQ</span>
                    <svg width="9" height="5" viewBox="0 0 9 5" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M0.883789 1L4.38379 4L7.88379 0.999999" stroke="#EF6C1E" stroke-linecap="round" stroke-linejoin="round"/>
                    </svg>
                </button>
                <ul class="mobile_menu__nav_list" :class="accordion == 'FAQ' ? 'active' : ''">
                    <li>
                        <a href="#">Личные кабинеты</a>
                    </li>
                    <li>
                        <a href="#">Цены и остатки</a>
                    </li>
                    <li>
                        <a href="#">Ассортимент</a>
                    </li>
                    <li>
                        <a href="#">Подключение</a>
                    </li>
                    <li>
                        <a href="#">Аналитика</a>
                    </li>
                </ul>
            </li>
        </ul>
    </div>
</template>

<style>

</style>