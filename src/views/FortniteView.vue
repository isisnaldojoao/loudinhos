<script setup>
import { onMounted } from 'vue';
import 'bootstrap-icons/font/bootstrap-icons.css';
import AOS from 'aos';
import 'aos/dist/aos.css';

import instagram from '@/assets/instagram.svg';
import twich from '@/assets/twich.svg';
import youtube from '@/assets/youtube.svg';

const lineup = [
    {id:1, titles:'Nenhum até o momento'}
];

const players = [
    { id: 1, name: 'Diguera', image: 'https://yt3.googleusercontent.com/MTgGV5OWyzrcc4A5v4fRDdNz2W5tG4peRSyESSIv6ntWoyIfdJu6cIAL4tP_-yzLrzRaN2TU=s900-c-k-c0x00ffffff-no-rj', instagram: 'https://www.instagram.com/loud_diguera/', twitch: 'https://www.twitch.tv/diguera' },
    { id: 2, name: 'KINGBR', image: 'https://i.imgur.com/2dhf0IE.jpeg', instagram: 'https://www.instagram.com/loud_kingbr/', youtube: 'https://www.youtube.com/kingfps' },
    { id: 3, name: 'GABZERA', image: 'https://i.imgur.com/BxphVtI.jpeg', instagram: 'https://www.instagram.com/loud_gabzera/', twitch: 'https://www.twitch.tv/loud_gabzera' },
    { id: 4, name: 'NIGHT', image: 'https://i.imgur.com/8cb2zhQ.jpeg', instagram: 'https://www.instagram.com/loud_nightftn/', twitch: 'https://www.twitch.tv/nightftn/' },
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
            <div data-aos="fade-up" class="bg-zinc-900 mt-5 md:w-2/3 rounded-lg justify-center">
                <p class="text-white p-3 font-bold">FORTNITE</p>
            </div>
        </div>
        <div class="md:flex justify-center">
            <img data-aos="zoom-in" class="loudlol mt-2 rounded-lg" src="https://i.imgur.com/jFhjqAC.png" alt="LOUD Image">
        </div>
        <div class="md:flex justify-center">
            <div data-aos="fade-up" class="bg-zinc-900 mt-5 md:w-2/3 rounded-lg justify-center">
                <p class="text-white p-3 font-bold">PLAYERS</p>
            </div>
        </div>
        <div class="md:flex justify-center gap-5">
            <div v-for="(player, index) in players" :key="player.id"
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
                        <img :class="player.twitch ? 'bg-purple-700' : 'bg-red-700'" class="rounded-sm w-full h-6" :src="player.twitch ? twich : youtube" :alt="player.twitch ? 'Twitch' : 'YouTube'"/>
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
            <div v-for="lineup in lineup" :key="lineup.id"
                 data-aos="zoom-in"
                 class="text-center cursor-pointer">
                <i class="bi bi-trophy-fill text-7xl"></i>
                <p class="text-white font-bold">{{lineup.titles}}</p>
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