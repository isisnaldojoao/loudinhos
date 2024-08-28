<script setup>
import loudlol from '@/assets/loudlol.png'
import robo from '@/assets/loudlol/robo.jpeg'
import croc from '@/assets/loudlol/croc.jpeg'
import tin from '@/assets/loudlol/tin.jpg'
import route from '@/assets/loudlol/route.jpg'
import redbert from '@/assets/loudlol/redbert.jpg'
import 'bootstrap-icons/font/bootstrap-icons.css';

import instagram from '@/assets/instagram.svg';
import twitterx from '@/assets/twitter-x.svg';
</script>
<template>
    <main class="md:flex flex-col">
        <div class="md:flex justify-center">
            <div class="bg-zinc-900 mt-5 md: w-2/3 rounded-lg justify-center">
                <p class="text-white p-3 font-bold">LEAGUE OF LEGENDS</p>
                
            </div>
        </div>
        <div class=" md:flex justify-center">
            <img class="loudlol mt-2 rounded-lg" :src="loudlol">
        </div>
        <div class=" md:flex justify-center">
            <div class="bg-zinc-900 mt-5 md: w-2/3 rounded-lg justify-center">
                <p class="text-white p-3 font-bold">PLAYERS</p>
            </div>
        </div>
        <div class="md:flex justify-center gap-5">
            <div class="flex flex-col justify-center items-center mt-5 cursor-pointer">
                <img class="pro rounded-lg shadow-2xl " :src="robo">
                <p class="w-full bg-zinc-900 text-white font-bold rounded-sm text-center mt-2">ROBO</p>
                <div class="w-full flex">
                    <img class="bg-red-500 rounded-sm w-1/2 h-6" :src="instagram"/>
                    <img class="bg-black rounded-sm w-1/2 h-6"  :src="twitterx"/>
                </div>
            </div>

            <div class="flex flex-col justify-center items-center mt-5 cursor-pointer">
                <img class="pro rounded-lg shadow-2xl " :src="croc">
                <p class="w-full bg-zinc-900 text-white font-bold rounded-sm text-center mt-2">CROC</p>
                <div class="w-full flex">
                    <img class="bg-red-500 rounded-sm w-1/2 h-6" :src="instagram"/>
                    <img class="bg-black rounded-sm w-1/2 h-6"  :src="twitterx"/>
                </div>
            </div>

            <div class="flex flex-col justify-center items-center mt-5 cursor-pointer">
                <img class="pro rounded-lg shadow-2xl " :src="tin">
                <p class="w-full bg-zinc-900 text-white font-bold rounded-sm text-center mt-2">TINOWNS</p>
                <div class="w-full flex">
                    <img class="bg-red-500 rounded-sm w-1/2 h-6" :src="instagram"/>
                    <img class="bg-black rounded-sm w-1/2 h-6"  :src="twitterx"/>
                </div>
            </div>

            <div class="flex flex-col justify-center items-center mt-5 cursor-pointer">
                <img class="pro rounded-lg shadow-2xl " :src="route">
                <p class="w-full bg-zinc-900 text-white font-bold rounded-sm text-center mt-2">ROUTE</p>
                <div class="w-full flex">
                    <img class="bg-red-500 rounded-sm w-1/2 h-6" :src="instagram"/>
                    <img class="bg-black rounded-sm w-1/2 h-6"  :src="twitterx"/>
                </div>
            </div>

             <div class="flex flex-col justify-center items-center mt-5 cursor-pointer">
                <img class="pro rounded-lg shadow-2xl " :src="redbert">
                <p class="w-full bg-zinc-900 text-white font-bold rounded-sm text-center mt-2">REDBERT</p>
                <div class="w-full flex">
                    <img class="bg-red-500 rounded-sm w-1/2 h-6" :src="instagram"/>
                    <img class="bg-black rounded-sm w-1/2 h-6"  :src="twitterx"/>
                </div>
            </div>
        </div>
        <div class="md:flex justify-center">
            <div class="bg-zinc-900 mt-5 md: w-2/3 rounded-lg justify-center">
                <p class="text-white p-3 font-bold">TITULOS</p>
            </div>
        </div>
        <div class="md:flex justify-center gap-6">
            <div class="text-center cursor-pointer">
                <i class="bi bi-trophy-fill text-7xl "></i>
                <p class="text-white font-bold">CBLOL SPLIT 2022.2</p>
            </div>

            <div class="text-center cursor-pointer">
                <i class="bi bi-trophy-fill text-7xl "></i>
                <p class="text-white font-bold">CBLOL SPLIT 2023.1</p>
            </div>

            <div class="text-center cursor-pointer">
                <i class="bi bi-trophy-fill text-7xl "></i>
                <p class="text-white font-bold">CBLOL SPLIT 2023.2</p>
            </div>

            <div class="text-center cursor-pointer">
                <i class="bi bi-trophy-fill text-7xl "></i>
                <p class="text-white font-bold">CBLOL SPLIT 2024.1</p>
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