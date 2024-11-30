<script setup>
import { ref } from 'vue';
import 'bootstrap-icons/font/bootstrap-icons.css';

import instagram from '@/assets/instagram.svg';
import twich from '@/assets/twich.svg';
import youtube from '@/assets/youtube.svg';

import { onMounted } from 'vue';
import AOS from 'aos';
import 'aos/dist/aos.css';


const activeTab = ref(0);
const tabs = ref([
  { 
    title: 'League of Legends', 
    cards: [
        { header: 'LTA Sul', team1: 'LOUD LEAGUE OF LEGENDS',team2: '',day: 'Março a Junho', hours: '1 etapa' },
        { header: 'LTA Sul', team1: 'LOUD LEAGUE OF LEGENDS',team2: '',day: 'Julho a Setembro', hours: '2 etapa' },
        { header: 'LTA Sul', team1: 'LOUD LEAGUE OF LEGENDS',team2: '',day: 'Outubro', hours: 'Torneio de Promoção da Primeira Divisão' },
    ]
  },
  { 
    title: 'VALORANT', 
    cards: [
        { header: 'VCT', team1: 'LOUD VALORANT',team2: '',day: '16/01/2025', hours: 'Kickoff Americas' },
        { header: 'VCT ', team1: 'LOUD VALORANT',team2: '',day: '20/02/2025 à 02/03/2025', hours: 'Masters Bangkok' },
        { header: 'VCT ', team1: 'LOUD VALORANT',team2: '',day: '22/03/2025 à 16/05/2025', hours: 'VCT Stage 1' },
        { header: 'VCT ', team1: 'LOUD VALORANT',team2: '',day: '07/06/2025 à 22/06/2025', hours: 'Masters Toronto' },
        { header: 'VCT ', team1: 'LOUD VALORANT',team2: '',day: '16/07/2025 à 29/08/2025', hours: 'Stage 2' },
        { header: 'VCT ', team1: 'LOUD VALORANT',team2: '',day: '12/09/2025 à 05/10/2025', hours: 'Champions Paris' },
    ]
  },
]);

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
    <main class="md:flex flex-col min-h-screen">
      <div class="md:flex justify-center tabs-container w-full">
        <div class="flex-col w-full max-w-4xl">
          <h1 class="text-green-400 my-5 text-2xl">Calendário das modalidades em que a <strong>LOUD</strong> estará presente:</h1>
          <div class="tabs flex gap-5 mb-6">
            <button 
              v-for="(tab, index) in tabs" 
              :key="index"
              @click="activeTab = index"
              :class="{ 'bg-green-700': activeTab === index, 'bg-green-500': activeTab !== index }"
              class="hover:bg-green-700 text-white font-bold py-3 px-6 rounded text-lg"
            >
              {{ tab.title }}
            </button>
          </div>
          <div class="tab-content">
            <div data-aos="fade-up" 
                data-aos-easing="linear"
                data-aos-duration="1500"
            class="flex flex-col gap-6">
              <div v-for="(card, cardIndex) in tabs[activeTab].cards" :key="cardIndex" class=" w-full flex flex-col lg:flex-row bg-green-600 rounded-lg shadow-md overflow-hidden">
                <div v-if="card.image" class="h-48 lg:h-auto lg:w-48 flex-none bg-cover bg-center " :style="{ backgroundImage: `url(${card.image})` }" :title="card.title">
                </div>
                <div class="p-4 flex flex-col justify-between leading-normal">
                  <div>
                    <div class="text-gray-100">{{ card.day }}</div>
                    <div class="text-white font-bold text-xl mb-2">{{ card.header }} | {{ card.hours ? `  ${card.hours}` : '' }}</div>
                    <p v-if="card.team1" class="text-white text-base">{{ card.team1 }}</p>
                    <p v-if="card.team2" class="text-white text-base">{{ card.team2 }}</p>
                  </div> 
                </div>
              </div>
            </div>
          </div>
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