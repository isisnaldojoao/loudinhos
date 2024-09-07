<script setup>
import 'bootstrap-icons/font/bootstrap-icons.css';

import instagram from '@/assets/instagram.svg';
import twich from '@/assets/twich.svg';
import youtube from '@/assets/youtube.svg';


const lineup =[
    {id:1,titles:'VCT 2022 Brazil Stage 1 Challengers'},
    {id:2,titles:'VCT 2022: Brazil Stage 2 Challengers'},
    {id:3,titles:'VALORANT Champions 2022'},
    {id:5,titles:'VCT 2023: Americas League'}
]


</script>
<template>
    <main class="md:flex flex-col">
        <div class="md:flex justify-center">
            <div class="bg-zinc-900 mt-5 md: w-2/3 rounded-lg justify-center">
                <p class="text-white p-3 font-bold">VALORANT</p>
                
            </div>
        </div>
        <div class="md:flex justify-center">
            <img class="loudlol mt-2 rounded-lg" :src="'https://files.bo3.gg/uploads/news/49426/title_image/960x480-ac7717eedb9074b53198db50b9e2c9a1.webp'" alt="LOUD Image">
        </div>
        <div class=" md:flex justify-center">
            <div class="bg-zinc-900 mt-5 md: w-2/3 rounded-lg justify-center">
                <p class="text-white p-3 font-bold">PLAYERS</p>
            </div>
        </div>
        <div class="md:flex justify-center gap-5">
            <div class="flex flex-col justify-center items-center mt-5 cursor-pointer">
                <img class="pro rounded-lg shadow-2xl " :src="'https://static.valorantzone.gg/news/2022/04/01105441/pancada-loud.jpg'">
                <p class="w-full bg-zinc-900 text-white font-bold rounded-sm text-center mt-2">pANcada</p>
                <div class="w-full flex">
                    <!-- Envolvendo a imagem do Instagram com um link -->
                    <a :href="'https://www.instagram.com/pancadafps/'" target="_blank" class="w-1/2">
                    <img class="bg-red-500 rounded-sm w-full h-6" :src="instagram" alt="Instagram"/>
                    </a>
                    
                    <!-- Envolvendo a imagem do Twitter com um link -->
                    <a :href="'https://www.twitch.tv/pancadalv'" target="_blank" class="w-1/2">
                    <img class="bg-purple-700 rounded-sm w-full h-6" :src="twich" alt="Twitter"/>
                    </a>
                </div>
            </div>

            <div class="flex flex-col justify-center items-center mt-5 cursor-pointer">
                <img class="pro rounded-lg shadow-2xl " :src="'https://prosettings.net/cdn-cgi/image/dpr=1%2Cf=auto%2Cfit=cover%2Cgravity=auto%2Cheight=217%2Cq=80%2Csharpen=1%2Cwidth=217/wp-content/uploads/cauanzin.png'">
                <p class="w-full bg-zinc-900 text-white font-bold rounded-sm text-center mt-2">CAUANZIN</p>
                <div class="w-full flex">
                    <!-- Envolvendo a imagem do Instagram com um link -->
                    <a :href="'https://www.instagram.com/cauanzinpd/'" target="_blank" class="w-1/2">
                    <img class="bg-red-500 rounded-sm w-full h-6" :src="instagram" alt="Instagram"/>
                    </a>
                    
                    <!-- Envolvendo a imagem do Twitter com um link -->
                    <a :href="'https://www.twitch.tv/cauanzinvlr'" target="_blank" class="w-1/2">
                    <img class="bg-purple-700 rounded-sm w-full h-6" :src="twich" alt="Twitter"/>
                    </a>
                </div>
            </div>

            <div class="flex flex-col justify-center items-center mt-5 cursor-pointer">
                <img class="pro rounded-lg shadow-2xl " :src="'https://prosettings.net/cdn-cgi/image/dpr=1%2Cf=auto%2Cfit=cover%2Cgravity=auto%2Cheight=217%2Cq=80%2Csharpen=1%2Cwidth=217/wp-content/uploads/tuyz.png'">
                <p class="w-full bg-zinc-900 text-white font-bold rounded-sm text-center mt-2">TUYZ</p>
                <div class="w-full flex">
                    <!-- Envolvendo a imagem do Instagram com um link -->
                    <a :href="'https://www.instagram.com/loud_tuyz1/'" target="_blank" class="w-1/2">
                    <img class="bg-red-500 rounded-sm w-full h-6" :src="instagram" alt="Instagram"/>
                    </a>
                    
                    <!-- Envolvendo a imagem do Twitter com um link -->
                    <a :href="'https://www.twitch.tv/tuyzvlr'" target="_blank" class="w-1/2">
                    <img class="bg-purple-700 rounded-sm w-full h-6" :src="twich" alt="Twitter"/>
                    </a>
                </div>
            </div>

            <div class="flex flex-col justify-center items-center mt-5 cursor-pointer">
                <img class="pro rounded-lg shadow-2xl " :src="'https://prosettings.net/wp-content/uploads/less.png'">
                <p class="w-full bg-zinc-900 text-white font-bold rounded-sm text-center mt-2">LESS</p>
                <div class="w-full flex">
                    <!-- Envolvendo a imagem do Instagram com um link -->
                    <a :href="'https://www.instagram.com/lessvlr/'" target="_blank" class="w-1/2">
                    <img class="bg-red-500 rounded-sm w-full h-6" :src="instagram" alt="Instagram"/>
                    </a>
                    
                    <!-- Envolvendo a imagem do Twitter com um link -->
                    <a :href="'https://www.twitch.tv/lessvlr'" target="_blank" class="w-1/2">
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