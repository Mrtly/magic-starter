<template>
  <div class="min-h-screen w-full bg-slate-100 p-6">
    <div class="mt-10 flex flex-col items-center gap-10 text-center">
      <h1 class="text-3xl font-semibold text-teal-900">
        Vue + Vite + TS starter
      </h1>
      <Button @click="increment">count is {{ count }}</Button>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";
import Button from "./components/Button.vue";

const count = ref(0);

function increment() {
  count.value++;
}
</script>
