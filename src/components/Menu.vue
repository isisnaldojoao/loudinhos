<script setup>
import { ref } from 'vue';
import logoImage from '@/assets/logo.png';
import Button from './Button.vue';
import { RouterLink } from 'vue-router';
import x from '../assets/x.svg'
import list from '../assets/list.svg'

const open = ref(false);
const btn = ref(false)

const toggleOpen = () => {
  open.value = !open.value;
  btn.value = !btn.value;
};
</script>

<template>
  <nav class="bg-zinc-900 text-gray-100 py-3.5 px-6 shadow md:flex justify-between items-center relative sticky ">
    <div>
      <img :src="logoImage" class="logo cursor-pointer animate-bounce" alt="Logo"/>
    </div>

    <button class="toggleButon absolute md:hidden right-6 top-1.5 text-4xl focus:outline-none" @click="toggleOpen" aria-expanded="open.toString()">
      <img :src="[open ? x : list ]"/>
    </button>

    <ul class="md:flex md:items-center md:px-0 px-3 md:pb-0 pb-10 md:static absolute bg-zinc-900 w-full top-14 md:top-auto duration-500 ease-in-out mt-2" :class="[open ? 'left-0' : 'left-[-100%]']">
      <li class="md:mx-4 md:my-0 my-6">
        <RouterLink to="/" class="text-xl font-semibold hover:text-green-400">INICIO</RouterLink>
      </li>
      <li class="md:mx-4 md:my-0 my-6">
        <RouterLink to="/modalidades" class="text-xl font-semibold hover:text-green-400">MODALIDADES</RouterLink>
      </li>
      <li class="md:mx-4 md:my-0 my-6">
        <RouterLink to="/redes-sociais" class="text-xl font-semibold hover:text-green-400">REDES SOCIAIS</RouterLink>
      </li>
      <li class="md:mx-4 md:my-0 my-6">
      </li>
    </ul>
  </nav>
</template>

<style scoped>
.logo {
  width: 40px;
  animation: bounce 2s infinite;
}

.toggleButon img{
    width: 40px;
    fill: white;
    
}

</style>
