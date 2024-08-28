<script>
import { useRouter } from 'vue-router'

export default {
  setup() {
    const router = useRouter()

    const goToLol = () => {
      router.push('/lol')
    }

    return {
      goToLol
    }
  }
}
</script>

<template>
<main class="md:flex flex-col h-screen">
    <div class="md:flex justify-center">
        <div class="bg-zinc-900 mt-5 md: w-2/3 rounded-lg justify-center">
            <p class="text-white p-3 font-bold">MODALIDADES</p>
        </div>
    </div>
    <section class="flex justify-center w-full">
        <div class=" sm:grid grid-cols-2 gap-2 ">
            <div class="bg-zinc-900 rounded-lg w-[500px] mt-5 cursor-pointer hover:border hover:border-green-600" @click="goToLol">
                <p class="p-5 text-center text-white font-bold" >EA FC 24</p>
            </div>

            <div class="bg-zinc-900 rounded-lg w-[500px] mt-5 cursor-pointer hover:border hover:border-green-600" @click="goToLol">
                <p class="p-5 text-center text-white font-bold">FORTNITE</p>
            </div>

            <div class="bg-zinc-900 rounded-lg w-[500px] mt-5 cursor-pointer hover:border hover:border-green-600" @click="goToLol">
                <p class="p-5 text-center text-white font-bold">FREE FIRE MOBILE</p>
            </div>

            <div class="bg-zinc-900 rounded-lg w-[500px] mt-5 cursor-pointer hover:border hover:border-green-600" @click="goToLol">
                <p class="p-5 text-center text-white font-bold">FREE FIRE EMULADOR</p>
            </div>

            <div class="bg-zinc-900 rounded-lg w-[500px] mt-5 cursor-pointer hover:border hover:border-green-600" @click="goToLol">
                <p class="p-5 text-center text-white font-bold">LEAGUE OF LEGENDS</p>
            </div>

            <div class="bg-zinc-900 rounded-lg w-[500px] mt-5 cursor-pointer hover:border hover:border-green-600" @click="goToLol">
                <p class="p-5 text-center text-white font-bold">LEAGUE OF LEGENDS ACADEMY</p>
            </div>

            <div class="bg-zinc-900 rounded-lg w-[500px] mt-5 cursor-pointer hover:border hover:border-green-600" @click="goToLol">
                <p class="p-5 text-center text-white font-bold">ROCKET LEAGUE</p>
            </div>

            <div class="bg-zinc-900 rounded-lg w-[500px] mt-5 cursor-pointer hover:border hover:border-green-600" @click="goToLol">
                <p class="p-5 text-center text-white font-bold">VALORANT </p>
            </div>
            
            <div class="bg-zinc-900 rounded-lg w-[500px] mt-5 cursor-pointer hover:border hover:border-green-600" @click="goToLol">
                <p class="p-5 text-center text-white font-bold">VALORANT INCLUSIVO</p>
            </div>
        </div>
    </section>
</main>
</template>

<style>

</style>
