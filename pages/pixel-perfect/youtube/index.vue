<template>
  <div class="flex flex-row w-full">
    <div style="position: fixed; height: 100vh; width: 72px; background-color: #202020">
      <div class="flex flex-col" style="padding-top: 56px">
        <div
          v-for="(item, index) in categories"
          :key="index"
          style="height: 72px"
          class="flex flex-col flex items-center justify-center cursor-pointer"
        >
          <i :class="item.icon"></i>
          <p class="text-xs">{{ item.name }}</p>
        </div>
      </div>
    </div>
    <div class="w-full">
      <div style="position: fixed; margin-left: 72px" class="w-full">
        <div
          class="w-full flex flex-col justify-center"
          style="
            height: 56px;
            border-bottom: 1px solid #373737;
            background-color: #202020;
          "
        >
          <div class="w-full flex justify-center items-center gap-3 px-6">
            <div class="flex w-1/2">
              <input
                type="text"
                placeholder="Pesquisar"
                style="height: 34px; border: solid 1px #303030; background-color: #121212"
                class="w-full px-2 py-2"
              />
              <button
                style="background-color: #303030"
                class="flex items-center px-2 rounded-r-[2px]"
              >
                <i class="mdi mdi-magnify"></i>
              </button>
            </div>
          </div>
        </div>
        <div
          class="w-full"
          style="
            height: 56px;
            border-bottom: 1px solid #373737;
            background-color: #202020;
          "
        >
          <div class="h-full flex items-center gap-3 pl-6">
            <div
              v-for="(item, index) in [
                'todos',
                'ação',
                'aventura',
                'científico',
                'drama',
                'herói',
                'medieval',
              ]"
              :key="index"
            >
              <div
                class="rounded-full flex items-center cursor-pointer"
                style="
                  background-color: #373737;
                  border: 1px #4b4b4b solid;
                  padding-left: 12px;
                  padding-right: 12px;
                  height: 32px;
                  font-size: 14px;
                "
              >
                {{ item }}
              </div>
            </div>
          </div>
        </div>
      </div>
      <div style="margin-top: 112px; margin-left: 72px">
        <div class="p-6">
          <div
            class="px-6 lg:px-12 xl:px-0 grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-4"
          >
            <div v-for="(item, index) in titles" :key="index">
              <div class="grid grid-cols-1 gap-2">
                <img :src="`/pixel-perfect/youtube/${item}`" alt="" />
                <p class="font-semibold">{{ item.replace(".jpg", "")  }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup lang="ts">
const categories = [
  { icon: "mdi mdi-home", name: "inicio" },
  { icon: "mdi mdi-sword-cross", name: "ação" },
  { icon: "mdi mdi-image-filter-hdr", name: "aventura" },
  { icon: "mdi mdi-atom", name: "científico" },
  { icon: "mdi mdi-drama-masks", name: "drama" },
  { icon: "mdi mdi-account-cowboy-hat", name: "herói" },
  { icon: "mdi mdi-castle", name: "medieval" },
];

const titles = [
  `007 - Sem Tempo para Morrer.jpg`,
  `1917.jpg`,
  `A Lenda do Cavaleiro Verde.jpg`,
  `Advogado do Diabo.jpg`,
  `Amor Além da Vida.jpg`,
  `Anônimo.jpg`,
  `Aventuras de um matemático.jpg`,
  `Belfast.jpg`,
  `Caça às Bruxas.jpg`,
  `Cruzada.jpg`,
  `Deuses do Egito.jpg`,
  `Druk - Mais Uma Rodada.jpg`,
  `Duna.jpg`,
  `Eternos.jpg`,
  `Homem Aranha - Sem Volta Pra Casa.jpg`,
  `Infinito.jpg`,
  `John Wick 2 - Um Novo Dia para Matar.jpg`,
  `John Wick 3 - Parabellum.jpg`,
  `King's Man - A Origem.jpg`,
  `King's Man - Serviço Secreto.jpg`,
  `Macbeth - Ambição & Guerra.jpg`,
  `Matrix - Ressurections.jpg`,
  `Minority Report - A Nova Lei.jpg`,
  `O Jogo da Imitação.jpg`,
  `Parasita.jpg`,
  `Rambo - Até o Fim.jpg`,
  `Robin Hood - A Origem.jpg`,
  `Seven - Os Sete Crimes Capitais.jpg`,
  `Tenet.jpg`,
  `Vidro.jpg`,
  `Zodiaco.jpg`,
  `Ófelia.jpg`,
];
</script>
<style>
html {
  width: 100%;
  height: 100%;
  color: white;
  font-family: "IBM Plex Sans", sans-serif;
  background-color: #181818;
}

canvas {
  position: fixed !important;
}
</style>
