<script setup>
import { onMounted } from 'vue';
import AOS from 'aos';
import 'aos/dist/aos.css';

import 'bootstrap-icons/font/bootstrap-icons.css';

import instagram from '@/assets/instagram.svg';
import twich from '@/assets/twich.svg';
import youtube from '@/assets/youtube.svg';

const lineup = [
    {id:1, titles:'Nenhum até o momento'},
];

const players = [
    { name: 'WAVED', image: 'https://i.imgur.com/WrvkaQe.jpeg', instagram: 'https://www.instagram.com/loud_waved/', youtube: 'https://www.youtube.com/results?search_query=loud+waved' },
    { name: 'ATNG', image: 'https://i.imgur.com/SCfUxyD.jpeg', instagram: 'https://www.instagram.com/loud_antg/', twitch: 'https://www.twitch.tv/antgvlr' },
    { name: 'MANDZIN', image: 'https://i.imgur.com/pbOiHr3.jpeg', instagram: 'https://www.instagram.com/loud_mandzin/', twitch: 'https://www.twitch.tv/m4ndzin' },
    { name: 'BLU', image: 'https://i.imgur.com/QUi9qxi.jpeg', instagram: 'https://www.instagram.com/loud_bluvlr/', twitch: 'twitch.tv/bluvlr' },
    { name: 'NATASHA', image: 'https://i.imgur.com/a1WxdMo.jpeg', instagram: 'https://www.instagram.com/loud_natasha05/', twitch: 'https://www.twitch.tv/natasha05' },
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
                <p class="text-white p-3 font-bold">VALORANT INCLUSIVO</p>
            </div>
        </div>
        <div class="md:flex justify-center">
            <img data-aos="zoom-in" class="loudlol mt-2 rounded-lg" src="https://i.imgur.com/jtfC76X.png" alt="LOUD Image">
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
                    <a :href="player.instagram" target="_blank" class="w-1/2">
                        <img class="bg-red-500 rounded-sm w-full h-6" :src="instagram" alt="Instagram"/>
                    </a>
                    <a :href="player.twitch || player.youtube" target="_blank" class="w-1/2">
                        <img :class="{'bg-purple-700': player.twitch, 'bg-red-700': player.youtube}" class="rounded-sm w-full h-6" :src="player.twitch ? twich : youtube" :alt="player.twitch ? 'Twitch' : 'YouTube'"/>
                    </a>
                </div>
            </div>
        </div>
        <div class="md:flex justify-center">
            <div data-aos="fade-up" class="bg-zinc-900 mt-5 md:w-2/3 rounded-lg justify-center">
                <p class="text-white p-3 font-bold">TITULOS</p>
            </div>
        </div>
        <div class="md:flex justify-center gap-6">
            <div v-for="item in lineup" :key="item.id"
                 data-aos="zoom-in"
                 class="text-center cursor-pointer">
                <i class="bi bi-trophy-fill text-7xl"></i>
                <p class="text-white font-bold">{{item.titles}}</p>
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