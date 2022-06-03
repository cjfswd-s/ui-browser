import { NuxtLink } from '../.nuxt/components';
<script setup lang="ts">
const ROUTER = useRouter();

const CLEAR_ROUTES_ATTRIBUTES = ROUTER.options.routes.map(
  // @ts-ignore
  ({ children, alias, file, ...item }) => item
);

const ROUTES_BY_CATEGORY = CLEAR_ROUTES_ATTRIBUTES.filter((item) =>
  ["free-style", "pixel-perfect"].some(
    (category) =>
      item.name.toString().includes(category) &&
      item.path.toString().split("/").length - 1 > 1
  )
);
type IGroupedRoute = {
  [key in "free-style" | "pixel-perfect"]: {
    name: string;
    path: string;
  }[];
};

const replaceAllHyphens = (valueToReplace: string) => {
  return valueToReplace.replace(/-/g, " ");
};

const ROUTES_GROUPED = ROUTES_BY_CATEGORY.reduce((previous, current) => {
  const key = current.path.toString().split("/")[1];
  // short circuit evaluation
  (previous[key] = previous[key] || []).push(current); // assigns [] to previous[key] if previous[key] is falsy, if is true continue previous value + push reduce current
  return previous;
}, {}) as IGroupedRoute;
</script>
<template>
  <div class="flex flex-col justify-center items-center leading-tight p-4">
    <div class="flex flex-col gap-8 w-full max-w-[800px]">
      <div class="flex flex-col w-full">
        <h1 class="text-3xl">UI - Browser</h1>
        <p>free creation and pixel perfect cloning web browser layouts.</p>
        <span class="text-sm"
          >by
          <NuxtLink to="https://github.com/cjfswd" target="_blank" class="text-[#8AB4F8] cursor-pointer hover:underline"
            >@cjfswd</NuxtLink
          ></span
        >
      </div>
      <div class="flex flex-col gap-4">
        <div v-for="(list, key) in ROUTES_GROUPED" :key="key" class="flex flex-col gap-2">
          <h2 :to="`/${key}`" class="text-2xl">{{ replaceAllHyphens(key) }}<br /></h2>
          <div class="grid grid-cols-3 gap-4">
            <NuxtLink v-for="(item, index) in list" :key="index" :to="item.path">
            <img :src="`/${item.path.toString().split('/')[2]}.jpg`" alt="" class="rounded-lg shadow shadow-md mb-2"/>
            <p class="text-sm">{{ replaceAllHyphens(item.path.toString().split("/")[2]) }}</p>
            </NuxtLink>
          </div>
        </div>
      </div>
      <div>
        <p>
          check the details at github
          <NuxtLink to="https://github.com/cjfswd/ui-browser" target="_blank" class="text-[#8AB4F8] cursor-pointer hover:underline"
            >repository</NuxtLink
          >
        </p>
      </div>
    </div>
  </div>
</template>
