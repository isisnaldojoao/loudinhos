<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Menu from './components/Menu.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <div class="bg-zinc-700 min-h-screen">
    <header >
      <Menu/>
    </header>
    
    <RouterView />
    <Footer/>
  </div>
  
</template>


<style >

</style>
