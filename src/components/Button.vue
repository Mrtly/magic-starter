<template>
  <button
    class="text-md w-fit cursor-pointer rounded px-4 py-2 bg-teal-700 tracking-wider text-white shadow transition-all duration-75 hover:shadow-lg active:scale-[.99] active:bg-teal-800"
    @click="handleClick"
  >
    <slot />
  </button>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "VueButton",
  emits: ["click"],
  computed: {},
  methods: {
    handleClick(event: Event) {
      this.$emit("click", event);
    },
  },
});
</script>
