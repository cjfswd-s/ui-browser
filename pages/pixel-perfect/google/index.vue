<script setup lang="ts">
let height = ref(0);

function resize() {
  height.value = innerHeight;
}

onMounted(() => {
  try {
    height.value = innerHeight;
    window.addEventListener("resize", resize);
  } catch (error) {
    console.log(error);
  }
});

onBeforeMount(() => {
  window.removeEventListener("resize", resize);
});
</script>
<template>
  <div
    :style="`height:${height}px`"
    class="flex flex-col flex justify-between items-center bg-[#202124]"
  >
    <navbar class="w-full flex flex-row justify-end items-center gap-4 p-4 text-[#E2E2E3]"
      ><span>Gmail</span><span>Imagens</span
      ><i class="mdi mdi-dots-grid text-[26px] cursor-pointer" />
      <img
        class="w-[38px] rounded-full cursor-pointer"
        src="data:image/jpeg;base64,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"
        alt=""
    /></navbar>
    <main
      class="flex flex-col justify-center items-center w-full max-w-[700px] gap-8 px-4"
    >
      <img
        class="lnXdpd"
        alt="Google"
        height="92"
        src="https://www.google.com/images/branding/googlelogo/1x/googlelogo_light_color_272x92dp.png"
        srcset="
          https://www.google.com/images/branding/googlelogo/1x/googlelogo_light_color_272x92dp.png 1x,
          https://www.google.com/images/branding/googlelogo/1x/googlelogo_light_color_272x92dp.png 2x
        "
        width="272"
        data-atf="1"
        data-frt="0"
      />
      <div class="w-full rounded-full border-[1px] border-[#5F6368] p-1">
        <div class="flex flex-row items-center px-2 h-[34px] w-full gap-4">
          <i class="mdi mdi-magnify text-[20px] text-[#5F6368] cursor-pointer" /><input
            type="text"
            class="w-full bg-transparent"
          /><img src="" alt="" /><span></span>
        </div>
      </div>
      <div class="flex flex-row gap-4">
        <button>Pesquisa Google</button><button>Estou com sorte</button>
      </div>
      <div class="text-[#BDC1C6] text-sm">
        Disponibilizado pelo Google em:
        <span class="text-[#8AB4F8] cursor-pointer hover:underline">English</span>
      </div>
    </main>
    <footer class="w-full bg-[#171717] text-[#9AA0A6]">
      <div class="w-full px-8 py-3 border-b border-[#212327]"><span>Brasil</span></div>
      <div class="w-full px-8 py-3 flex flex-row justify-between">
        <div class="flex flex-row gap-8">
          <span>Sobre</span> <span>Publicidade</span> <span>Negócios</span>
          <span>Como funciona a Pesquisa</span>
        </div>
        <div class="flex flex-row gap-8">
          <span>Privacidade</span> <span>Termos</span> <span>Configurações</span>
        </div>
      </div>
    </footer>
  </div>
</template>
<style scoped>
button {
  background-color: #303134;
  @apply py-2 px-4 rounded border-[1px] border-[#202124] hover:border-[#5F6368];
}

span {
  @apply cursor-pointer hover:underline;
}

/* Remove the stupid outer glow in Webkit */
input:focus {
  outline: 0;
}
</style>
