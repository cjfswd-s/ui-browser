<template>
  <div class="bg-black text-white">
    <div
      class="backdrop-blur-sm text-white flex w-full h-[480px] justify-center items-center bg-[#D51D31]"
    >
      <div class="relative px-4 w-full md:max-w-[1100px]" style="z-index: 99">
        <div
          class="w-full flex flex-col-reverse md:flex-row justify-center items-center gap-4"
        >
          <div
            class="w-full flex flex-col justify-center items-center sm:w-1/2 sm:text-6xl font-bold leading-tight"
          >
            <div class="w-min flex flex-col">
              <p class="w-min whitespace-nowrap mdi mdi-filmstrip text-5xl sm:text-6xl">
                CINEVIX
              </p>
              <p class="w-min whitespace-nowrap text-2xl sm:text-4xl">MEIA ENTRADA</p>
              <p class="w-min whitespace-nowrap text-2xl sm:text-4xl">TODOS OS DIAS</p>
              <p class="w-min whitespace-nowrap sm:text-3xl font-semibold">
                em qualquer filme,
              </p>
              <p class="w-min whitespace-nowrap sm:text-3xl font-semibold">
                sala ou sessão.
              </p>
              <p class="w-min whitespace-nowrap text-xs font-semibold">
                ingresso a R$20,00.
              </p>
            </div>
          </div>
          <div class="shadow shadow-drop-lg hidden md:w-1/2 md:block sm:rounded-lg">
            <img
              class="border-2 border-[#D51D31] rounded-lg"
              src="/free-style/cinevix/cinema3.jpeg"
              alt=""
            />
          </div>
        </div>
      </div>
      <div
        class="fixed w-full h-full"
        style="
          z-index: 0;
          filter: blur(3px);
          background-size: cover;
          background: url('https://www.venturashopping.com.br/wp-content/uploads/2021/10/Banner_Cinema.png');
        "
      ></div>
    </div>
    <div class="flex flex-col w-full justify-center items-center">
      <div
        class="flex flex-col justify-center gap-4 max-w-[1100px] min-h-[440px] py-[40px] px-6 mb:px-0"
      >
        <h2 class="text-4xl font-semibold">Em cartaz</h2>
        <div class="grid grid-cols-2 sm:grid-cols-3 lg:grid-cols-6 gap-4">
          <div
            class="flex flex-col gap-1 text-xs"
            v-for="(image, index) in [
              'drestranho.jpg',
              'sonic2.jpg',
              'morbius.jpg',
              'jujutsu.jpg',
              'medidaprovisoria.jpg',
              'cidade.jpg',
            ]"
          >
            <img
              class="rounded-lg"
              :src="`/free-style/cinevix/${image}`"
              :key="index"
              alt=""
            />
            <div class="grid grid-cols-2 text-center gap-1">
              <nuxt-link
                to="/"
                class="flex flex-row gap-0.5 p-0.5 justify-center bg-[#D51D31] rounded"
                ><span class="mdi mdi-play-box"></span>trailer</nuxt-link
              >
              <nuxt-link
                to="/"
                class="flex flex-row gap-0.5 p-0.5 justify-center bg-[#D51D31] rounded"
                ><span class="mdi mdi-clock-outline"></span> sessões</nuxt-link
              >
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="flex flex-col w-full justify-center items-center">
      <div
        class="flex flex-col justify-center gap-4 max-w-[1100px] min-h-[440px] py-[40px] px-6 mb:px-0"
      >
        <h2 class="text-4xl font-semibold">Salas</h2>
        <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
          <div
            class="flex flex-col gap-1 text-xs"
            v-for="(room, index) in [
              { scr: 'cinema2.png', label: 'Little Room' },
              { scr: 'cinema.jpg', label: 'Big Room' },
            ]"
          >
            <img
              class="rounded-lg"
              :src="`/free-style/cinevix/${room.scr}`"
              :key="index"
              alt=""
            />
            <div class="text-center gap-1">
              <nuxt-link
                to="/"
                class="flex flex-row gap-0.5 p-0.5 justify-center bg-[#D51D31] rounded"
              >
                {{ room.label }}</nuxt-link
              >
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="flex flex-col w-full items-center justify-center">
      <div class="flex flex-col w-full max-w-[1100px] py-[40px] px-6 mb:px-0">
        <div class="grid grid-cols-2">
          <div class="flex flex-col gap-6 leading-[1.1]">
            <h2 class="text-2xl font-semibold">Contato</h2>
            <div class="flex flex-col gap-[5px]">
              <p><i class="mdi mdi-instagram" /> instagram</p>
              <p><i class="mdi mdi-facebook" /> facebook</p>
              <p><i class="mdi mdi-youtube" /> youtube</p>
            </div>
          </div>
          <div class="flex flex-col gap-6 leading-[1.1]">
            <h2 class="text-2xl font-semibold">Mapa do site</h2>
            <div class="flex flex-col gap-[5px]">
              <p>ínicio</p>
              <p>em cartaz</p>
              <p>trailers</p>
              <p>sessões</p>
              <p>contato</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
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
