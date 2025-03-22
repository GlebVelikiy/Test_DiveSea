<template>
    <div class="slider__container">
        <h1 class="slider__heading">
            Weekly - Top NFT
        </h1>
        <infinite-slide-bar 
            :barStyle="{ background: '#f1f1f1'}" 
            duration="30s"  
            class="slider__slides-container"
        >
            <div 
                ref="slides" 
                class="slider__slides" 
                :style="{ transform: `translateX(${currentOffset}px)`}"
            >
                <AppNFT 
                    v-for="item in items" 
                    :key="item.id" 
                    :item="item"
                >
                </AppNFT>
            </div>
        </infinite-slide-bar>
        <div class="slider__controls">
            <button 
                class="slider__button" 
                @click="handleLeftClick" 
                aria-label="Перейти назад"
            >
                <img src="@/assets/LeftArrow.png" alt="">
            </button>
            <div class="slider__line"></div>
            <button 
                class="slider__button" 
                @click="handleRightClick" 
                aria-label="Перейти вперед"
            >
                <img src="@/assets/RightArrow.png" alt="">
            </button>
        </div>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import InfiniteSlideBar from 'vue3-infinite-slide-bar';
import AppNFT from './AppNFT.vue';

const items = [
    { id: 1, name: 'Sun-Glass', image: require('@/assets/NFT1.png'), currentBid: 1.75},
    { id: 2, name: 'Moon-Light', image: require('@/assets/NFT2.png'), currentBid: 2.5},
    { id: 3, name: 'Star-Dust', image: require('@/assets/NFT3.png'), currentBid: 3.0},
    { id: 4, name: 'Ocean-Wave', image: require('@/assets/NFT4.png'), currentBid: 4.25},
    { id: 5, name: 'Sun-Glass', image: require('@/assets/NFT1.png'), currentBid: 1.75},
    { id: 6, name: 'Moon-Light', image: require('@/assets/NFT2.png'), currentBid: 2.5},
    { id: 7, name: 'Star-Dust', image: require('@/assets/NFT3.png'), currentBid: 3.0},
    { id: 8, name: 'Ocean-Wave', image: require('@/assets/NFT4.png'), currentBid: 4.25}
]

const slideWidth = 300;
const currentIndex = ref(0);
const currentOffset = ref(0);

function handleLeftClick() {
    currentOffset.value += slideWidth;
}

function handleRightClick() {
    currentOffset.value -= slideWidth;
}
</script>

<style scoped lang="scss">
@import '@/assets/styles/slider.scss';
</style>