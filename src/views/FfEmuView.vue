<script setup>
import 'bootstrap-icons/font/bootstrap-icons.css';

import instagram from '@/assets/instagram.svg';
import twich from '@/assets/twich.svg';
import youtube from '@/assets/youtube.svg'

const lineup =[
    {id:1,titles:'La Copa'},
    {id:2,titles:'NFA SEASON 4'},
    {id:3,titles:'NFA SEASON 3'},
    {id:4,titles:'NFA SEASON 2'},
    {id:5,titles:'Copa General'},
    {id:6,titles:'LIGA W1N'},
    {id:7,titles:'TALENTS SEASON 1'},
    {id:8,titles:'TALENTS SEASON 2'},
    {id:9,titles:'Liga BDL Season 1 Series A'},
    {id:10,titles:'Super Liga GrandSlam'},
    {id:11,titles:'Champions League LBR'},
    {id:12,titles:'Naguará Cup Emulador'},
    {id:13,titles:'LIGA LBR SEASON 5'},
    {id:14,titles:'CHAMPIONS LBR'},
    {id:15,titles:'LIGA LBR SEASON 2'},
    {id:16,titles:'Max FyreLeague'},

]

</script>
<template>
    <main class="md:flex flex-col">
        <div class="md:flex justify-center">
            <div class="bg-zinc-900 mt-5 md: w-2/3 rounded-lg justify-center">
                <p class="text-white p-3 font-bold">FREE FIRE EMULADOR</p>
                
            </div>
        </div>
        <div class="md:flex justify-center">
            <img class="loudlol mt-2 rounded-lg" :src="'https://cdn.statically.io/img/theradioativo.com.br/wp-content/uploads/2024/04/Snapinsta.app_432774332_18163771450307496_5851913643991579570_n_1080.jpg?quality=100&f=auto'" alt="LOUD Image">
        </div>
        <div class=" md:flex justify-center">
            <div class="bg-zinc-900 mt-5 md: w-2/3 rounded-lg justify-center">
                <p class="text-white p-3 font-bold">PLAYERS</p>
            </div>
        </div>
        <div class="md:flex justify-center gap-5">
            <div class="flex flex-col justify-center items-center mt-5 cursor-pointer">
                <img class="pro rounded-lg shadow-2xl " :src="'https://yt3.googleusercontent.com/ChpkJtS5YwjOO0n_iz6TOej-sdGg0lDV_Eui5dRSEqwVJOaBsxaAFF0IzHBdSFsaK_0QkP2z=s900-c-k-c0x00ffffff-no-rj'">
                <p class="w-full bg-zinc-900 text-white font-bold rounded-sm text-center mt-2">BAK</p>
                <div class="w-full flex">
                    <a :href="'https://www.instagram.com/bak'" target="_blank" class="w-1/2">
                    <img class="bg-red-500 rounded-sm w-full h-6" :src="instagram" alt="Instagram"/>
                    </a>
                    
                    <a :href="'https://www.youtube.com/@BAK8X'" target="_blank" class="w-1/2">
                    <img class="bg-red-700 rounded-sm w-full h-6" :src="youtube" alt="Twitter"/>
                    </a>
                </div>
            </div>

            <div class="flex flex-col justify-center items-center mt-5 cursor-pointer">
                <img class="pro rounded-lg shadow-2xl " :src="'https://img.wattpad.com/cover/326148874-352-k519315.jpg'">
                <p class="w-full bg-zinc-900 text-white font-bold rounded-sm text-center mt-2">THURZIN</p>
                <div class="w-full flex">
                    <a :href="'https://www.instagram.com/loud_thurzin/'" target="_blank" class="w-1/2">
                    <img class="bg-red-500 rounded-sm w-full h-6" :src="instagram" alt="Instagram"/>
                    </a>
                    
                    <a :href="'https://www.youtube.com/@LOUD_THURZIN'" target="_blank" class="w-1/2">
                    <img class="bg-red-700 rounded-sm w-full h-6" :src="youtube" alt="Twitter"/>
                    </a>
                </div>
            </div>

            <div class="flex flex-col justify-center items-center mt-5 cursor-pointer">
                <img class="pro rounded-lg shadow-2xl " :src="'https://yt3.googleusercontent.com/90PznGfdglhRwFOlFMJ_iabX5rhFBeDOb1__IQZaj5bV6w__nO_DSrOlpWv0NNk1cC6kTtBPmVg=s900-c-k-c0x00ffffff-no-rj'">
                <p class="w-full bg-zinc-900 text-white font-bold rounded-sm text-center mt-2">JAYA</p>
                <div class="w-full flex">
                    <!-- Envolvendo a imagem do Instagram com um link -->
                    <a :href="'https://www.instagram.com/loud_jaya1/'" target="_blank" class="w-1/2">
                    <img class="bg-red-500 rounded-sm w-full h-6" :src="instagram" alt="Instagram"/>
                    </a>
                    
                    <!-- Envolvendo a imagem do Twitter com um link -->
                    <a :href="'https://www.youtube.com/@LOUD_JAYA'" target="_blank" class="w-1/2">
                    <img class="bg-red-700 rounded-sm w-full h-6" :src="youtube" alt="Twitter"/>
                    </a>
                </div>
            </div>

            <div class="flex flex-col justify-center items-center mt-5 cursor-pointer">
                <img class="pro rounded-lg shadow-2xl " :src="'https://i.imgur.com/tlXS3jg.jpeg'">
                <p class="w-full bg-zinc-900 text-white font-bold rounded-sm text-center mt-2">LIGEIRIN</p>
                <div class="w-full flex">
                    <!-- Envolvendo a imagem do Instagram com um link -->
                    <a :href="'https://www.instagram.com/loud_ligerin1/'" target="_blank" class="w-1/2">
                    <img class="bg-red-500 rounded-sm w-full h-6" :src="instagram" alt="Instagram"/>
                    </a>
                    
                    <!-- Envolvendo a imagem do Twitter com um link -->
                    <a :href="'https://www.youtube.com/@ligerinffx'" target="_blank" class="w-1/2">
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
        <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 justify-center">
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