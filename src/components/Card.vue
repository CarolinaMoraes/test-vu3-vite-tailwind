<template>
  <div class="rounded-card mx-auto mt-3 py-5 px-5">
    <div>
      <p class="font-semibold">Should this be something useful?</p>
      <p>
        Lorem ipsum dolor sit amet consectetur, adipisicing elit. Reprehenderit
        inventore doloribus repellat reiciendis quod autem expedita voluptates
        saepe rerum! Optio repudiandae quisquam quibusdam impedit nobis
        inventore doloribus nihil laborum itaque.
      </p>
    </div>

    <div class="mt-3">
      <p class="font-semibold">This will show an injected value:</p>
      {{ injectedMessage }}
    </div>
  </div>
</template>
<script setup>
import { inject } from "vue";

const injectedMessage = inject("injectedValue", "Just a default message");
</script>
