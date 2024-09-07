<script setup>
import 'bootstrap-icons/font/bootstrap-icons.css';

import instagram from '@/assets/instagram.svg';
import twich from '@/assets/twich.svg';
import youtube from '@/assets/youtube.svg';


const lineup =[
    {id:1,titles:'Nenhum até o momento'}
]


</script>
<template>
    <main class="md:flex flex-col">
        <div class="md:flex justify-center">
            <div class="bg-zinc-900 mt-5 md: w-2/3 rounded-lg justify-center">
                <p class="text-white p-3 font-bold">FREE FIRE</p>
                
            </div>
        </div>
        <div class="md:flex justify-center">
            <img class="loudlol mt-2 rounded-lg" :src="'https://assets.gamearena.gg/wp-content/uploads/2024/06/11100012/LOUD-Free-Fire-EWC-2024-1024x689.png'" alt="LOUD Image">
        </div>
        <div class=" md:flex justify-center">
            <div class="bg-zinc-900 mt-5 md: w-2/3 rounded-lg justify-center">
                <p class="text-white p-3 font-bold">PLAYERS</p>
            </div>
        </div>
        <div class="md:flex justify-center gap-5">
            <div class="flex flex-col justify-center items-center mt-5 cursor-pointer">
                <img class="pro rounded-lg shadow-2xl " :src="'https://dl.dir.freefiremobile.com/common/Local/VN/Esports/05_2022/IMG_PLAYER_FFWS/LOUD.CAUAN7.png'">
                <p class="w-full bg-zinc-900 text-white font-bold rounded-sm text-center mt-2">CAUAN7</p>
                <div class="w-full flex">
                    <!-- Envolvendo a imagem do Instagram com um link -->
                    <a :href="'https://www.instagram.com/loud_cauan/'" target="_blank" class="w-1/2">
                    <img class="bg-red-500 rounded-sm w-full h-6" :src="instagram" alt="Instagram"/>
                    </a>
                    
                    <!-- Envolvendo a imagem do Twitter com um link -->
                    <a :href="'https://www.youtube.com/@LOUDcauan'" target="_blank" class="w-1/2">
                    <img class="bg-red-700 rounded-sm w-full h-6" :src="youtube" alt="Twitter"/>
                    </a>
                </div>
            </div>

            <div class="flex flex-col justify-center items-center mt-5 cursor-pointer">
                <img class="pro rounded-lg shadow-2xl " :src="'https://dl.dir.freefiremobile.com/common/Local/VN/Esports/05_2022/IMG_PLAYER_FFWS/LOUD.LOST21.png'">
                <p class="w-full bg-zinc-900 text-white font-bold rounded-sm text-center mt-2">LOST</p>
                <div class="w-full flex">
                    <!-- Envolvendo a imagem do Instagram com um link -->
                    <a :href="'https://www.instagram.com/loud_lost/'" target="_blank" class="w-1/2">
                    <img class="bg-red-500 rounded-sm w-full h-6" :src="instagram" alt="Instagram"/>
                    </a>
                    
                    <!-- Envolvendo a imagem do Twitter com um link -->
                    <a :href="'https://www.youtube.com/@loudlost212'" target="_blank" class="w-1/2">
                    <img class="bg-red-700 rounded-sm w-full h-6" :src="youtube" alt="Twitter"/>
                    </a>
                </div>
            </div>

            <div class="flex flex-col justify-center items-center mt-5 cursor-pointer">
                <img class="pro rounded-lg shadow-2xl " :src="'https://i.imgur.com/nBYRhrw.jpeg'">
                <p class="w-full bg-zinc-900 text-white font-bold rounded-sm text-center mt-2">DRAXX</p>
                <div class="w-full flex">
                    <!-- Envolvendo a imagem do Instagram com um link -->
                    <a :href="'https://www.instagram.com/loud_draxx7/'" target="_blank" class="w-1/2">
                    <img class="bg-red-500 rounded-sm w-full h-6" :src="instagram" alt="Instagram"/>
                    </a>
                    
                    <!-- Envolvendo a imagem do Twitter com um link -->
                    <a :href="'https://www.youtube.com/results?search_query=loud+draxx'" target="_blank" class="w-1/2">
                    <img class="bg-red-700 rounded-sm w-full h-6" :src="youtube" alt="Twitter"/>
                    </a>
                </div>
            </div>

            <div class="flex flex-col justify-center items-center mt-5 cursor-pointer">
                <img class="pro rounded-lg shadow-2xl " :src="'https://theradioativo.com.br/wp-content/uploads/2024/01/IMG_0394.jpeg'">
                <p class="w-full bg-zinc-900 text-white font-bold rounded-sm text-center mt-2">YAGO</p>
                <div class="w-full flex">
                    <!-- Envolvendo a imagem do Instagram com um link -->
                    <a :href="'https://www.instagram.com/loud.yago/'" target="_blank" class="w-1/2">
                    <img class="bg-red-500 rounded-sm w-full h-6" :src="instagram" alt="Instagram"/>
                    </a>
                    
                    <!-- Envolvendo a imagem do Twitter com um link -->
                    <a :href="'https://www.youtube.com/results?search_query=loud+yago'" target="_blank" class="w-1/2">
                    <img class="bg-red-700 rounded-sm w-full h-6" :src="youtube" alt="Twitter"/>
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