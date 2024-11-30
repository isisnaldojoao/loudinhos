<script setup>
import { ref } from 'vue';
import logoImage from '@/assets/logo.png';
import { RouterLink } from 'vue-router';
import x from '../assets/x.svg'
import list from '../assets/list.svg';
import { House } from 'lucide-vue-next';
import { Swords } from 'lucide-vue-next';
import { CalendarFold } from 'lucide-vue-next';

import { onMounted } from 'vue';
import AOS from 'aos';
import 'aos/dist/aos.css';

const open = ref(false);
const btn = ref(false)

const toggleOpen = () => {
  open.value = !open.value;
  btn.value = !btn.value;
};

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
  <nav data-aos="fade-down"
      data-aos-easing="linear"
      data-aos-duration="1500"
      class="bg-zinc-900 text-gray-100 py-3.5 px-6 shadow sticky top-0">
    <div class="max-w-6xl mx-auto flex flex-col items-center relative">

      <div class="mb-4 ">
        <img :src="logoImage" class="logo cursor-pointer " alt="Logo"/>
      </div>


      <div class="w-full flex justify-center">
        <ul class="hidden md:flex md:items-center">
          <li class="mx-4">
            <RouterLink to="/" class="flex items-center gap-2 text-xl font-semibold hover:text-green-400">INICIO <House/></RouterLink>
          </li>
          <li class="mx-4">
            <RouterLink to="/modalidades" class="flex items-center gap-2 text-xl font-semibold hover:text-green-400">MODALIDADES <Swords/></RouterLink>
          </li>
          <li class="mx-4">
            <RouterLink to="/agenda" class="flex items-center gap-2 text-xl font-semibold hover:text-green-400">AGENDA <CalendarFold /></RouterLink>
          </li>
        </ul>
      </div>

      <button class="toggleButon absolute md:hidden right-6 top-1.5 text-4xl focus:outline-none" @click="toggleOpen" aria-expanded="open.toString()">
        <img :src="[open ? x : list ]"/>
      </button>


      <div class="md:hidden w-full" v-show="open">
        <ul class="flex flex-col items-center py-4">
          <li class="my-2">
            <RouterLink to="/" class="flex items-center gap-2 text-xl font-semibold hover:text-green-400">INICIO <House/></RouterLink>
          </li>
          <li class="my-2">
            <RouterLink to="/modalidades" class="flex items-center gap-2 text-xl font-semibold hover:text-green-400">MODALIDADES <Swords/></RouterLink>
          </li>
          <li class="my-2">
            <RouterLink to="/agenda" class="flex items-center gap-2 text-xl font-semibold hover:text-green-400">AGENDA <CalendarFold /></RouterLink>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<style scoped>
.logo {
  width: 200px;
}

.toggleButon img {
  width: 40px;
  fill: white;
}

@keyframes bounce {
  0%, 100% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(-10px);
  }
}
</style>