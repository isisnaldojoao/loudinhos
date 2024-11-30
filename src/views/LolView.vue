<script setup>
import { onMounted } from 'vue';
import AOS from 'aos';
import 'aos/dist/aos.css';

import loudlol from '@/assets/loudlol.png'
import robo from '@/assets/loudlol/robo.jpeg'
import croc from '@/assets/loudlol/croc.jpeg'
import tin from '@/assets/loudlol/tin.jpg'
import route from '@/assets/loudlol/route.jpg'
import redbert from '@/assets/loudlol/redbert.jpg'
import 'bootstrap-icons/font/bootstrap-icons.css';

import instagram from '@/assets/instagram.svg';
import twitterx from '@/assets/twitter-x.svg';

const players = [
    { name: 'ROBO', image: robo },
    { name: 'CROC', image: croc },
    { name: 'TINOWNS', image: tin },
    { name: 'ROUTE', image: route },
    { name: 'REDBERT', image: redbert },
];

const titles = [
    'CBLOL SPLIT 2022.2',
    'CBLOL SPLIT 2023.1',
    'CBLOL SPLIT 2023.2',
    'CBLOL SPLIT 2024.1',
];

onMounted(() => {
  AOS.init({
    duration: 1000,
    easing: 'ease-in-out',
    once: true,
    offset: 50,
  });
});
</script>

<template>
    <main class="md:flex flex-col">
        <div class="md:flex justify-center">
            <div data-aos="fade-down" class="bg-zinc-900 mt-5 md:w-2/3 rounded-lg justify-center">
                <p class="text-white p-3 font-bold">LEAGUE OF LEGENDS</p>
            </div>
        </div>
        <div class="md:flex justify-center">
            <img data-aos="zoom-in" class="loudlol mt-2 rounded-lg" :src="loudlol">
        </div>
        <div class="md:flex justify-center">
            <div data-aos="fade-up" class="bg-zinc-900 mt-5 md:w-2/3 rounded-lg justify-center">
                <p class="text-white p-3 font-bold">PLAYERS</p>
            </div>
        </div>
        <div class="md:flex justify-center gap-5">
            <div v-for="(player, index) in players" :key="index"
                 data-aos="fade-right"
                 :data-aos-delay="index * 100"
                 class="flex flex-col justify-center items-center mt-5 cursor-pointer">
                <img class="pro rounded-lg shadow-2xl" :src="player.image">
                <p class="w-full bg-zinc-900 text-white font-bold rounded-sm text-center mt-2">{{ player.name }}</p>
                <div class="w-full flex">
                    <img class="bg-red-500 rounded-sm w-1/2 h-6" :src="instagram"/>
                    <img class="bg-black rounded-sm w-1/2 h-6" :src="twitterx"/>
                </div>
            </div>
        </div>
        <div class="md:flex justify-center">
            <div data-aos="fade-up" class="bg-zinc-900 mt-5 md:w-2/3 rounded-lg justify-center">
                <p class="text-white p-3 font-bold">TITULOS</p>
            </div>
        </div>
        <div class="md:flex justify-center gap-6">
            <div v-for="(title, index) in titles" :key="index"
                 data-aos="zoom-in"
                 :data-aos-delay="index * 100"
                 class="text-center cursor-pointer">
                <i class="bi bi-trophy-fill text-7xl"></i>
                <p class="text-white font-bold">{{ title }}</p>
            </div>
        </div>
    </main>
</template>

<style scoped>
.loudlol{
    width: 1000px;
    height: 400px;
    object-fit: cover;
}
.pro{
    width: 180px;
    height: 200px;
}
</style>