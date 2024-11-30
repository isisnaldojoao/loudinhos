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
    { id: 1, name: 'CAUAN7', image: 'https://dl.dir.freefiremobile.com/common/Local/VN/Esports/05_2022/IMG_PLAYER_FFWS/LOUD.CAUAN7.png', instagram: 'https://www.instagram.com/loud_cauan/', youtube: 'https://www.youtube.com/@LOUDcauan' },
    { id: 2, name: 'LOST', image: 'https://dl.dir.freefiremobile.com/common/Local/VN/Esports/05_2022/IMG_PLAYER_FFWS/LOUD.LOST21.png', instagram: 'https://www.instagram.com/loud_lost/', youtube: 'https://www.youtube.com/@loudlost212' },
    { id: 3, name: 'DRAXX', image: 'https://i.imgur.com/nBYRhrw.jpeg', instagram: 'https://www.instagram.com/loud_draxx7/', youtube: 'https://www.youtube.com/results?search_query=loud+draxx' },
    { id: 4, name: 'YAGO', image: 'https://theradioativo.com.br/wp-content/uploads/2024/01/IMG_0394.jpeg', instagram: 'https://www.instagram.com/loud.yago/', youtube: 'https://www.youtube.com/results?search_query=loud+yago' },
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
                <p class="text-white p-3 font-bold">FREE FIRE</p>
            </div>
        </div>
        <div class="md:flex justify-center">
            <img data-aos="zoom-in" class="loudlol mt-2 rounded-lg" src="https://assets.gamearena.gg/wp-content/uploads/2024/06/11100012/LOUD-Free-Fire-EWC-2024-1024x689.png" alt="LOUD Image">
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
                    <a :href="player.youtube" target="_blank" class="w-1/2">
                        <img class="bg-red-700 rounded-sm w-full h-6" :src="youtube" alt="YouTube"/>
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