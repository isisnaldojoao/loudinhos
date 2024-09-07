<script setup>
import 'bootstrap-icons/font/bootstrap-icons.css';

import instagram from '@/assets/instagram.svg';
import twich from '@/assets/twich.svg';
import youtube from '@/assets/youtube.svg';


const lineup =[
    {id:1,titles:'Nenhum até o momento'},
]


</script>
<template>
    <main class="md:flex flex-col">
        <div class="md:flex justify-center">
            <div class="bg-zinc-900 mt-5 md: w-2/3 rounded-lg justify-center">
                <p class="text-white p-3 font-bold">VALORANT INCLUSIVO</p>
                
            </div>
        </div>
        <div class="md:flex justify-center">
            <img class="loudlol mt-2 rounded-lg" :src="'https://i.imgur.com/jtfC76X.png'" alt="LOUD Image">
        </div>
        <div class=" md:flex justify-center">
            <div class="bg-zinc-900 mt-5 md: w-2/3 rounded-lg justify-center">
                <p class="text-white p-3 font-bold">PLAYERS</p>
            </div>
        </div>
        <div class="md:flex justify-center gap-5">
            <div class="flex flex-col justify-center items-center mt-5 cursor-pointer">
                <img class="pro rounded-lg shadow-2xl " :src="'https://i.imgur.com/WrvkaQe.jpeg'">
                <p class="w-full bg-zinc-900 text-white font-bold rounded-sm text-center mt-2">WAVED</p>
                <div class="w-full flex">
                    <!-- Envolvendo a imagem do Instagram com um link -->
                    <a :href="'https://www.instagram.com/loud_waved/'" target="_blank" class="w-1/2">
                    <img class="bg-red-500 rounded-sm w-full h-6" :src="instagram" alt="Instagram"/>
                    </a>
                    
                    <!-- Envolvendo a imagem do Twitter com um link -->
                    <a :href="'https://www.youtube.com/results?search_query=loud+waved'" target="_blank" class="w-1/2">
                    <img class="bg-red-700 rounded-sm w-full h-6" :src="youtube" alt="Twitter"/>
                    </a>
                </div>
            </div>

            <div class="flex flex-col justify-center items-center mt-5 cursor-pointer">
                <img class="pro rounded-lg shadow-2xl " :src="'https://i.imgur.com/SCfUxyD.jpeg'">
                <p class="w-full bg-zinc-900 text-white font-bold rounded-sm text-center mt-2">ATNG</p>
                <div class="w-full flex">
                    <!-- Envolvendo a imagem do Instagram com um link -->
                    <a :href="'https://www.instagram.com/loud_antg/'" target="_blank" class="w-1/2">
                    <img class="bg-red-500 rounded-sm w-full h-6" :src="instagram" alt="Instagram"/>
                    </a>
                    
                    <!-- Envolvendo a imagem do Twitter com um link -->
                    <a :href="'https://www.twitch.tv/antgvlr'" target="_blank" class="w-1/2">
                    <img class="bg-purple-700 rounded-sm w-full h-6" :src="twich" alt="Twitter"/>
                    </a>
                </div>
            </div>

            <div class="flex flex-col justify-center items-center mt-5 cursor-pointer">
                <img class="pro rounded-lg shadow-2xl " :src="'https://i.imgur.com/pbOiHr3.jpeg'">
                <p class="w-full bg-zinc-900 text-white font-bold rounded-sm text-center mt-2">MANDZIN</p>
                <div class="w-full flex">
                    <!-- Envolvendo a imagem do Instagram com um link -->
                    <a :href="'https://www.instagram.com/loud_mandzin/'" target="_blank" class="w-1/2">
                    <img class="bg-red-500 rounded-sm w-full h-6" :src="instagram" alt="Instagram"/>
                    </a>
                    
                    <!-- Envolvendo a imagem do Twitter com um link -->
                    <a :href="'https://www.twitch.tv/m4ndzin'" target="_blank" class="w-1/2">
                    <img class="bg-purple-700 rounded-sm w-full h-6" :src="twich" alt="Twitter"/>
                    </a>
                </div>
            </div>

            <div class="flex flex-col justify-center items-center mt-5 cursor-pointer">
                <img class="pro rounded-lg shadow-2xl " :src="'https://i.imgur.com/QUi9qxi.jpeg'">
                <p class="w-full bg-zinc-900 text-white font-bold rounded-sm text-center mt-2">BLU</p>
                <div class="w-full flex">
                    <!-- Envolvendo a imagem do Instagram com um link -->
                    <a :href="'https://www.instagram.com/loud_bluvlr/'" target="_blank" class="w-1/2">
                    <img class="bg-red-500 rounded-sm w-full h-6" :src="instagram" alt="Instagram"/>
                    </a>
                    
                    <!-- Envolvendo a imagem do Twitter com um link -->
                    <a :href="'twitch.tv/bluvlr'" target="_blank" class="w-1/2">
                    <img class="bg-purple-700 rounded-sm w-full h-6" :src="twich" alt="Twitter"/>
                    </a>
                </div>
            </div>

            <div class="flex flex-col justify-center items-center mt-5 cursor-pointer">
                <img class="pro rounded-lg shadow-2xl " :src="'https://i.imgur.com/a1WxdMo.jpeg'">
                <p class="w-full bg-zinc-900 text-white font-bold rounded-sm text-center mt-2">NATASHA</p>
                <div class="w-full flex">
                    <!-- Envolvendo a imagem do Instagram com um link -->
                    <a :href="'https://www.instagram.com/loud_natasha05/'" target="_blank" class="w-1/2">
                    <img class="bg-red-500 rounded-sm w-full h-6" :src="instagram" alt="Instagram"/>
                    </a>
                    
                    <!-- Envolvendo a imagem do Twitter com um link -->
                    <a :href="'https://www.twitch.tv/natasha05'" target="_blank" class="w-1/2">
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