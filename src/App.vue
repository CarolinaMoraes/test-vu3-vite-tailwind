<template>
  <div class="mt-36">
    <div class="flex flex-auto gap-10 justify-center items-center mb-3">
      <a href="https://vitejs.dev" class="w-1/2 max-w-44" target="_blank">
        <img class="size-full" src="/vite.svg" alt="Vite logo" />
      </a>
      <a href="https://vuejs.org/" class="w-1/2 max-w-44" target="_blank">
        <img class="size-full" src="./assets/vue.svg" alt="Vue logo" />
      </a>
      <a href="https://vuejs.org/" class="w-1/2 max-w-44" target="_blank">
        <img class="size-full" src="./assets/tailwind.svg" alt="Vue logo" />
      </a>
    </div>
    <HelloWorld msg="Vite + Vue3 + Tailwind" />
  </div>
</template>
<script setup>
import { onMounted, provide } from "vue";
import HelloWorld from "./components/HelloWorld.vue";

onMounted(() => {
  provide("injectedValue", "This was injected from App.vue");
});
</script>
