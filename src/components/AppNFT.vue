<template>
    <div class="nft__container">
        <div class="nft__timer">{{ countdown }}</div>
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
import { defineProps, ref, onMounted, onUnmounted } from 'vue';

const props = defineProps(['item']);

const countdown = ref('07h 09m 12s');

let timer: number | undefined;

onMounted(() => {
  startCountdown();
});

onUnmounted(() => {
  clearInterval(timer);
});

function randomTime() {
  return Math.floor(Math.random() * (12000 - 3000 + 1)) + 3000;
}

function startCountdown() {
  let timeLeft = randomTime();

  timer = setInterval(() => {
    if (timeLeft > 0) {
      timeLeft--;
      updateCountdown(timeLeft);
    }
  }, 1000);
}

function updateCountdown(seconds: number) {
  const hours = Math.floor(seconds / 3600);
  const minutes = Math.floor((seconds % 3600) / 60);
  const remainingSeconds = seconds % 60;

  countdown.value = `${padZero(hours)}h ${padZero(minutes)}m ${padZero(remainingSeconds)}s`;
}

function padZero(num: number): string {
  return num.toString().padStart(2, '0');
}
</script>

<style scoped lang="scss">
@import '@/assets/styles/nft.scss';
</style>