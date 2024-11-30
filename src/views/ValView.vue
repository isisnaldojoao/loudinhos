<script setup>
import { onMounted } from 'vue';
import AOS from 'aos';
import 'aos/dist/aos.css';

import 'bootstrap-icons/font/bootstrap-icons.css';

import instagram from '@/assets/instagram.svg';
import twich from '@/assets/twich.svg';
import youtube from '@/assets/youtube.svg';

const lineup = [
    {id:1,titles:'VCT 2022 Brazil Stage 1 Challengers'},
    {id:2,titles:'VCT 2022: Brazil Stage 2 Challengers'},
    {id:3,titles:'VALORANT Champions 2022'},
    {id:5,titles:'VCT 2023: Americas League'}
];

const players = [
    { name: 'pANcada', image: 'https://static.valorantzone.gg/news/2022/04/01105441/pancada-loud.jpg', instagram: 'https://www.instagram.com/pancadafps/', twitch: 'https://www.twitch.tv/pancadalv' },
    { name: 'CAUANZIN', image: 'https://prosettings.net/cdn-cgi/image/dpr=1%2Cf=auto%2Cfit=cover%2Cgravity=auto%2Cheight=217%2Cq=80%2Csharpen=1%2Cwidth=217/wp-content/uploads/cauanzin.png', instagram: 'https://www.instagram.com/cauanzinpd/', twitch: 'https://www.twitch.tv/cauanzinvlr' },
    { name: 'TUYZ', image: 'https://prosettings.net/cdn-cgi/image/dpr=1%2Cf=auto%2Cfit=cover%2Cgravity=auto%2Cheight=217%2Cq=80%2Csharpen=1%2Cwidth=217/wp-content/uploads/tuyz.png', instagram: 'https://www.instagram.com/loud_tuyz1/', twitch: 'https://www.twitch.tv/tuyzvlr' },
    { name: 'LESS', image: 'https://prosettings.net/wp-content/uploads/less.png', instagram: 'https://www.instagram.com/lessvlr/', twitch: 'https://www.twitch.tv/lessvlr' },
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
                <p class="text-white p-3 font-bold">VALORANT</p>
            </div>
        </div>
        <div class="md:flex justify-center">
            <img data-aos="zoom-in" class="loudlol mt-2 rounded-lg" src="https://files.bo3.gg/uploads/news/49426/title_image/960x480-ac7717eedb9074b53198db50b9e2c9a1.webp" alt="LOUD Image">
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
                    <a :href="player.twitch" target="_blank" class="w-1/2">
                        <img class="bg-purple-700 rounded-sm w-full h-6" :src="twich" alt="Twitch"/>
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
            <div v-for="(item, index) in lineup" :key="item.id"
                 data-aos="zoom-in"
                 :data-aos-delay="index * 100"
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