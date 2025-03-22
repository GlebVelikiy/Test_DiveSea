<template>
    <header class="header" :class="{'active' : isMobileMenuOpen}">
        <div class="header__container">
            <div class="header__logo">
                <img src="@/assets/Wave.png" alt="Logo" />
                <span class="header__logo-text">
                    DiveSea
                </span>
            </div>
    
            <button class="header__burger" :class="{ 'active' : isMobileMenuOpen}" @click="toggleMobileMenu">
                <span class="header__burger-line"></span>
                <span class="header__burger-line"></span>
                <span class="header__burger-line"></span>
            </button>
    
            <nav class="header__nav">
                <ul class="header__nav-list">
                    <li class="header__nav-item">
                        <a href="#" class="header__nav-link">
                            DISCOVER
                        </a>
                    </li>
                    <li class="header__nav-item">
                        <a href="#" class="header__nav-link">
                            CREATORS
                        </a>
                    </li>
                    <li class="header__nav-item">
                        <a href="#" class="header__nav-link">
                            SELL
                        </a>
                    </li>
                    <li class="header__nav-item">
                        <a href="#" class="header__nav-link">
                            STATS
                        </a>
                    </li>
                </ul>
            </nav>
        
            <button class="header__connect-btn">
                CONNECT WALLET
            </button>
        </div>

        <div class="mobile-menu" :class="{'active' : isMobileMenuOpen}">
            <ul class="mobile-menu__list">
                <li class="mobile-menu__item">
                    <a href="#" class="mobile-menu__link">
                        DISCOVER
                    </a>
                </li>
                <li class="mobile-menu__item">
                    <a href="#" class="mobile-menu__link">
                        CREATORS
                    </a>
                </li>
                <li class="mobile-menu__item">

                    <a href="#" class="mobile-menu__link">
                        SELL
                    </a>
                </li>
                <li class="mobile-menu__item">

                    <a href="#" class="mobile-menu__link">
                        STATS
                    </a>
                </li>
                <li class="mobile-menu__item">
                    <ul class="mobile-menu__contacts">
                        <li>
                            <a href="#" class="mobile-menu__link">
                                <img class="mobile-menu__img" src="@/assets/contacts/Instagram.png" alt="">
                            </a>
                        </li>
                        <li>

                            <a href="#" class="mobile-menu__link">
                                <img class="mobile-menu__img" src="@/assets/contacts/In.png" alt="">
                            </a>
                        </li>
                        <li>

                            <a href="#" class="mobile-menu__link">
                                <img class="mobile-menu__img" src="@/assets/contacts/Facebook.png" alt="">
                            </a>
                        </li>
                        <li>

                            <a href="#" class="mobile-menu__link">
                                <img class="mobile-menu__img" src="@/assets/contacts/Twitter.png" alt="">
                            </a>
                        </li>
                    </ul>
                </li>
            </ul>
            <button class="mobile-menu__connect-btn">
                CONNECT WALLET
            </button>
        </div>
    </header>
</template>

<script setup lang="ts">
import { ref, onMounted, onUnmounted } from 'vue';

const isMobileMenuOpen = ref(false);

const toggleMobileMenu = () => {
isMobileMenuOpen.value = !isMobileMenuOpen.value;
};

const handleResize = () => {
  if (window.innerWidth > 600) {
    isMobileMenuOpen.value = false;
  }
};

onMounted(() => {
  window.addEventListener('resize', handleResize);
});

onUnmounted(() => {
  window.removeEventListener('resize', handleResize);
});
</script>

<style scoped lang="scss">
@import '@/assets/styles/variables.scss';
@import '@/assets/styles/header.scss';
@import '@/assets/styles/mobile_menu.scss';
</style>