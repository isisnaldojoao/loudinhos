<script setup>
import loudinhosNews from  '@/assets/loudinhos_news.png';
import instagram from '@/assets/instagram.svg';
import tiktok from '@/assets/tiktok.svg';
import twitterx from '@/assets/twitter-x.svg';
import youtube from '@/assets/youtube.svg';
import twich from '@/assets/twich.svg';

</script>

<template>
  <main class="md:flex flex-col">
    <section class=" md:flex justify-center items-center mt-2 ">
      <div class="my-15 md:my-0">
        <img :src="loudinhosNews" class="rounded-lg mr-3"/>
      </div>

      <div>
        <div class="bg-green-600 md:h-[600px] p-5 rounded-lg ">
          <h3 class="text-gray-50 font-bold">JOGOS DE HOJE</h3>
          <div class="bg-zinc-900 md:p-2 mb-2 text-gray-50 duration-200 cursor-pointer rounded-lg hover:scale-110">
            <p>LEAGUE OF LEGENDS</p>
            <div class="bg-white h-0.5 w-full"></div>
            <p>LOUD X PAIN</p>
            <div class="md:flex ">
              <p>07/09/2024</p>
              <p>-</p>
              <p>13:30</p>
            </div>
            <div class="flex flex-col">
            <p>Assista agora:</p>
              <div class="flex">
                <div class="bg-red-700 w-1/2 h-8 flex justify-center items-center rounded-lg"><img :src="youtube"/></div>
                <div class="bg-purple-600 w-1/2 h-8  flex justify-center items-center rounded-lg"><img :src="twich"/></div>
              </div>
            </div>
          </div>

          <div class="bg-zinc-900 md:p-2 mb-2 text-gray-50 duration-200 cursor-pointer rounded-lg hover:scale-110">
            <p>LEAGUE OF LEGENDS</p>
            <div class="bg-white h-0.5 w-full"></div>
            <p>LOUD X PAIN</p>
            <div class="md:flex ">
              <p>07/09/2024</p>
              <p>-</p>
              <p>13:30</p>
            </div>
            <div class="flex flex-col">
            <p>Assista agora:</p>
              <div class="flex">
                <div class="bg-red-700 w-1/2 h-8 flex justify-center items-center rounded-lg"><img :src="youtube"/></div>
                <div class="bg-purple-600 w-1/2 h-8  flex justify-center items-center rounded-lg"><img :src="twich"/></div>
              </div>
            </div>
          </div>

          
      </div>
      
        
      

      </div>

    </section>

    <section class="flex flex-col justify-center items-center mt-2">
      <h1 class="bg-zinc-900 md:max-w-5xl w-full p-4 rounded-lg text-white font-semibold">REDES SOCIAIS</h1>
      <div class="grid grid-cols-1 sm:grid-cols-2 mt-4 gap-1 w-[1030px] px-2 ">
        <div class="flex flex-col mt-3 justify-center items-center bg-green-600 w-full md:w-[500px] h-[100px] rounded-lg duration-200 cursor-pointer hover:scale-110"> 
          <img :src="instagram" class="w-10 mb-2"/>
          <div class="bg-white h-0.5 w-full"></div>
          <p class="mt-2 text-white text-center">INSTAGRAM LOUDINHOS</p>
        </div>

        <div class="flex flex-col mt-3 justify-center items-center bg-green-600 w-full md:w-[500px] h-[100px] rounded-lg duration-200 cursor-pointer hover:scale-110"> 
          <img :src="twitterx" class="w-10 mb-2"/>
          <div class="bg-white h-0.5 w-full"></div>
          <p class="mt-2 text-white text-center">TWITTER LOUDINHOS</p>
        </div>

        <div class="flex flex-col mt-3 justify-center items-center bg-green-600 w-full md:w-[500px] h-[100px] rounded-lg duration-200 cursor-pointer hover:scale-110"> 
          <img :src="youtube" class="w-10 mb-2"/>
          <div class="bg-white h-0.5 w-full"></div>
          <p class="mt-2 text-white text-center">YOUTUBE LOUDINHOS</p>
        </div>

        <div class="flex flex-col mt-3 justify-center items-center bg-green-600 w-full md:w-[500px] h-[100px] rounded-lg duration-200 cursor-pointer hover:scale-110"> 
          <img :src="tiktok" class="w-10 mb-2"/>
          <div class="bg-white h-0.5 w-full"></div>
          <p class="mt-2 text-white text-center">TIKTOK LOUDINHOS</p>
        </div>
      </div>
    </section>

    <section class="flex flex-col justify-center items-center mt-2 ">
      <form action="mailto:loudinhosofc@gmail.com" method="post" enctype="text/plain"
      class="flex flex-col bg-zinc-900 md:max-w-5xl w-full p-4 rounded-lg text-white font-semibold"
      >
        <h1 class="text-2xl uppercase">Podemos melhorar em algo? Nos envie um feedback!</h1>
        <label>Seu email:</label>
        <input class="rounded-sm outline-none" type="email" id="email" name="email" required>

        <label for="message">Mensagem:</label>
        <textarea  id="message" name="message" rows="4" cols="50" required class="text-black rounded-sm outline-none"></textarea>

        <input class="bg-green-500 mt-5 rounded-sm cursor-pointer" type="submit" value="Enviar" >
      </form>
    </section>


  </main>
</template>
