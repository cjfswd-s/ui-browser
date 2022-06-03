<script setup lang="ts">
import { ref, onMounted, onBeforeMount } from "vue";

import fitty from "public/js/fitty.min.js";

let height = ref(0);

function resize() {
  height.value = innerHeight;
}

onMounted(() => {
  try {
    height.value = innerHeight;
    window.addEventListener("resize", resize);
    fitty(".fit", {
      minSize: 1,
      maxSize: 300,
    });
    fitty.fitAll();
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
    id="app"
    :style="`height:${height}px`"
    class="w-full flex flex-col items-center justify-center"
  >
    <div class="w-full max-w-xs flex flex-col flex-grow p-2 sm:px-0 sm:py-6 gap-4">
      <div
        class="animate__animated animate__fadeInLeft animate__slow grid grid-cols-10 gap-2"
      >
        <img src="/free-style/linktree/i.png" class="rounded col-span-3" />
        <div class="col-span-7 flex flex-col align-center justify-center leading-none">
          <div>
            <p class="fit"><sup>Castillo</sup><sub>Junior</sub></p>
          </div>
        </div>
      </div>
      <p
        class="animate__animated animate__fadeInRight animate__slow leading-tight text-sm"
      >
        Desenvolvedor JS/TS Full-Stack
        <br />Entusiasta de Design & Hardware <br />Gamer & Geek
        <br />
      </p>
      <FreestyleLinktreeMoleculeSite
        class="animate__animated animate__fadeInUp animate__slow"
      />
    </div>
  </div>
</template>
<style lang="scss">
@import url("/free-style/linktree/index.scss");

#app {
  background-color: black;
  color: white;
}
</style>
