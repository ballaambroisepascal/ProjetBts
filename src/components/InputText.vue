<template>
  <div class="flex flex-col items-center text-black">
      <input
          ref="myInput"
          type="text"
          :placeholder="placeholder"
          class="w-[97%] border-[1px] border-solid bg-white p-2 focus:outline-none rounded mt-6"
          data-test="inputText"
      >
  </div>
</template>

<script setup lang="ts">
import { defineProps } from 'vue';

defineProps({
  placeholder: {
    type: String,
    required: true
  },
})
</script>