<script setup>
import 'bootstrap-icons/font/bootstrap-icons.css';

import instagram from '@/assets/instagram.svg';
import twich from '@/assets/twich.svg';
import youtube from '@/assets/youtube.svg';


const lineup =[
    {id:1,titles:'CBOLAO 2022'}
]


</script>
<template>
    <main class="md:flex flex-col">
        <div class="md:flex justify-center">
            <div class="bg-zinc-900 mt-5 md: w-2/3 rounded-lg justify-center">
                <p class="text-white p-3 font-bold">ROCKET LEAGUE</p>
                
            </div>
        </div>
        <div class="md:flex justify-center">
            <img class="loudlol mt-2 rounded-lg" :src="'https://i.imgur.com/pfSJIDl.png'" alt="LOUD Image">
        </div>
        <div class=" md:flex justify-center">
            <div class="bg-zinc-900 mt-5 md: w-2/3 rounded-lg justify-center">
                <p class="text-white p-3 font-bold">PLAYERS</p>
            </div>
        </div>
        <div class="md:flex justify-center gap-5">
            <div class="flex flex-col justify-center items-center mt-5 cursor-pointer">
                <img class="pro rounded-lg shadow-2xl " :src="'https://pbs.twimg.com/media/GD6JdVfWEAAf39x?format=jpg&name=4096x4096'">
                <p class="w-full bg-zinc-900 text-white font-bold rounded-sm text-center mt-2">DROPPZ</p>
                <div class="w-full flex">
                    <!-- Envolvendo a imagem do Instagram com um link -->
                    <a :href="'https://www.instagram.com/loud_droppz/'" target="_blank" class="w-1/2">
                    <img class="bg-red-500 rounded-sm w-full h-6" :src="instagram" alt="Instagram"/>
                    </a>
                    
                    <!-- Envolvendo a imagem do Twitter com um link -->
                    <a :href="'https://www.twitch.tv/ddroppz'" target="_blank" class="w-1/2">
                    <img class="bg-purple-700 rounded-sm w-full h-6" :src="twich" alt="Twitter"/>
                    </a>
                </div>
            </div>

            <div class="flex flex-col justify-center items-center mt-5 cursor-pointer">
                <img class="pro rounded-lg shadow-2xl " :src="'https://i.imgur.com/RvQxGiL.jpeg'">
                <p class="w-full bg-zinc-900 text-white font-bold rounded-sm text-center mt-2">SAD</p>
                <div class="w-full flex">
                    <!-- Envolvendo a imagem do Instagram com um link -->
                    <a :href="'https://www.instagram.com/loud_sadd/'" target="_blank" class="w-1/2">
                    <img class="bg-red-500 rounded-sm w-full h-6" :src="instagram" alt="Instagram"/>
                    </a>
                    
                    <!-- Envolvendo a imagem do Twitter com um link -->
                    <a :href="'https://www.twitch.tv/sadd_rl'" target="_blank" class="w-1/2">
                    <img class="bg-purple-700 rounded-sm w-full h-6" :src="twich" alt="Twitter"/>
                    </a>
                </div>
            </div>

            <div class="flex flex-col justify-center items-center mt-5 cursor-pointer">
                <img class="pro rounded-lg shadow-2xl " :src="'https://i.imgur.com/YsZWK9L.jpeg'">
                <p class="w-full bg-zinc-900 text-white font-bold rounded-sm text-center mt-2">KLAUS</p>
                <div class="w-full flex">
                    <!-- Envolvendo a imagem do Instagram com um link -->
                    <a :href="'https://www.instagram.com/loud_klausrl/'" target="_blank" class="w-1/2">
                    <img class="bg-red-500 rounded-sm w-full h-6" :src="instagram" alt="Instagram"/>
                    </a>
                    
                    <!-- Envolvendo a imagem do Twitter com um link -->
                    <a :href="'https://www.twitch.tv/klausrl1'" target="_blank" class="w-1/2">
                    <img class="bg-purple-700 rounded-sm w-full h-6" :src="twich" alt="Twitter"/>
                    </a>
                </div>
            </div>

            
        </div>
        <div class="md:flex justify-center">
            <div class="bg-zinc-900 mt-5 md: w-2/3 rounded-lg justify-center">
                <p class="text-white p-3 font-bold">TITULOS</p>
            </div>
        </div>
        <div class="md:flex justify-center gap-6">
            <div
            v-for="lineup in lineup"
            :key="lineup.id"
            class="text-center cursor-pointer">
                <i class="bi bi-trophy-fill text-7xl "></i>
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