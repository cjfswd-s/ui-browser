<template>
  <div
    class="flex flex-col w-full h-[100vh] justify-center items-center text-white"
    :style="`background:url('/free-style/gaming-guest/${wallpaper}'); background-size: cover; background-position: center; -webkit-transition: background-image 0.5s ease-in-out;
transition: background-image 0.5s ease-in-out;`"
  >
    <div
      class="p-[1px] bg-gradient-to-r from-cyan-500 to-blue-500 rounded-lg shadow drop-shadow-lg"
    >
      <div
        class="flex flex-row justify-center items-center gap-8 py-2 px-3 pb-28 rounded-lg"
        style="
          background-color: black;
          background: url(/free-style/gaming-guest/controllers.jpg.png) black;
          background-size: contain;
          background-position: bottom;
          background-repeat: no-repeat;
        "
      >
        <div class="w-min flex self-stretch flex-col justify-between gap-4">
          <div class="flex flex-col justify-center items-strech">
            <p
              class="flex items-center whitespace-nowrap text-xl font-bold tracking-wide text-white"
            >
              <i class="mdi mdi-google-controller text-2xl" />&nbsp;GamingGUEST
            </p>
            <p
              class="whitespace-nowrap font-bold text-transparent bg-clip-text bg-gradient-to-r from-green-400 to-blue-600 leading-tight"
            >
              Alugue video-games
            </p>
            <p
              class="font-bold text-transparent bg-clip-text bg-gradient-to-r from-green-400 to-blue-600 leading-tight"
            >
              a baixo custo.
            </p>
            <p
              class="font-bold text-transparent bg-clip-text bg-gradient-to-r from-blue-400 to-green-600 leading-tight"
            >
              1 dia R$50
            </p>
            <p
              class="font-bold text-transparent bg-clip-text bg-gradient-to-r from-blue-400 to-green-600 leading-tight"
            >
              1 semana R$150
            </p>
            <p
              class="font-bold text-transparent bg-clip-text bg-gradient-to-r from-blue-400 to-green-600 leading-tight"
            >
              1 mês R$500
            </p>
            <p
              class="text-xs font-bold text-transparent bg-clip-text bg-gradient-to-r from-green-400 to-blue-600 leading-tight"
            >
              é simples, rápido e funcional.
            </p>
          </div>
          <img src="/free-style/gaming-guest/logosconsoles.png" alt="" />
          <div class="flex flex-col">
            <p
              class="whitespace-nowrap mdi mdi-whatsapp text-xs font-bold text-transparent bg-clip-text bg-gradient-to-r from-red-400 to-blue-600 leading-tight"
            >
              21 9 8888-7777
            </p>
            <p
              class="mdi mdi-instagram text-xs font-bold text-transparent bg-clip-text bg-gradient-to-r from-red-400 to-blue-600 leading-tight"
            >
              instragram
            </p>
            <p
              class="mdi mdi-facebook text-xs font-bold text-transparent bg-clip-text bg-gradient-to-r from-red-400 to-blue-600 leading-tight"
            >
              facebook
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup lang="ts">
import { ref, onMounted } from "vue";

let wallpaper = ref("forza.jpg");
let wallpaperList = [
  "blood.jpg",
  "decay.jpg",
  "halo.jpg",
  "horizon.jpg",
  "infamous.jpg",
  "sunset.jpg",
  "the last.jpg",
  "gears.jpg",
  "god.png",
  "forza.jpg",
];

function sleep(ms) {
  return new Promise((resolve) => setTimeout(resolve, ms));
}

async function infiniteWallpaper() {
  for (let i = 0; i < wallpaperList.length; i++) {
    await sleep(3000);
    wallpaper.value = wallpaperList[i];
  }
  infiniteWallpaper();
}

onMounted(() => {
  infiniteWallpaper();
});
</script>
<style scoped>
.text-shadow {
  text-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.text-shadow-md {
  text-shadow: 0 4px 8px rgba(0, 0, 0, 0.12), 0 2px 4px rgba(0, 0, 0, 0.08);
}

.text-shadow-lg {
  text-shadow: 0 15px 30px rgba(0, 0, 0, 0.11), 0 5px 15px rgba(0, 0, 0, 0.08);
}

.text-shadow-none {
  text-shadow: none;
}
</style>
