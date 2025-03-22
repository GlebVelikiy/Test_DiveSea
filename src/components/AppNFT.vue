<template>
    <div class="nft__container">
        <img :src="item.image" alt="" class="nft__img">
        <h3 class="nft__heading">
            {{ item.name }}
        </h3>
        <span class="nft__text">
            Current bid
        </span>
        <div class="nft__bottom">
            <div class="nft__price">
                <img src="@/assets/ethereum.png" alt="" class="nft__price-img">
                <span class="nft__price-text">
                    {{ item.currentBid }}
                </span>
            </div>
            <button class="nft__button">
                PLACE BID
            </button>
        </div>
    </div>
</template>

<script setup lang="ts">
import { defineProps } from 'vue';

defineProps(['item'])
</script>

<style scoped lang="scss">
@import '@/assets/styles/nft.scss';
</style>