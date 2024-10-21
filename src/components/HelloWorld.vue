<template>
  <h1 class="font-bold text-center">{{ msg }}</h1>

  <div class="card text-center">
    <div class="mt-3">
      <button
        class="bg-purple-600 px-5 py-2 rounded drop-shadow-sm hover:bg-purple-700 mb-3"
        type="button"
        @click="count++"
      >
        count is {{ count }}
      </button>

      <p class="text-purple-400">{{ evenNumberText }}</p>

      <div class="w-2/3 mx-auto">
        <Card />
        <div class="md:flex gap-5">
          <TestimonialCard v-for="i in 3" :key="i" />
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>
import { ref, computed } from "vue";
import Card from "./Card.vue";
import TestimonialCard from "./TestimonialCard.vue";

defineProps({
  msg: String,
});

const count = ref(0);

const evenNumberText = computed(() => {
  return count.value % 2 === 0 ? "It's even" : "It's odd";
});
</script>
