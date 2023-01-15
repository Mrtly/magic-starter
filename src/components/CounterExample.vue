<template>
  <div class="text-xl mb-5">{{ msg }}</div>
  <button
    @click="increment"
    class="
      mt-4
      uppercase
      font-bold
      tracking-widest
      px-8
      py-2
      rounded-full
      bg-gray-600
      text-white
      max-w-max
      shadow-sm
      hover:shadow-lg
      focus:outline-none
    "
  >
    click
  </button>
  <div class="mt-4 m-auto text-xl font-semibold tracking-wider text-green-600">
    count is: {{ count }}
  </div>
  <button
    @click="reset"
    class="
      mt-8
      px-4
      py-1
      rounded-full
      border
      border-gray-300
      text-gray-500
      max-w-max
      shadow-sm
      hover:shadow-md
      focus:outline-none
    "
  >
    reset
  </button>
</template>

<script setup lang="ts">
import { ref } from "vue";

defineProps({
  msg: { type: String, default: "vite starter" },
});

let count: number = ref("0");

function increment() {
  count.value++;
}

function reset() {
  count.value = 0;
}
</script>
