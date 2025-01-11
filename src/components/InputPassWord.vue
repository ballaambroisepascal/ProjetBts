<template>
  <div class="relative w-full text-black">
    <input
        type="password"
        :placeholder="placeholder"
        class="w-[97%] border-[1px] bg-white p-2 focus:outline-none rounded mt-3"
    >
  </div>
</template>

<script setup lang="ts">
import {defineProps, ref} from 'vue';
defineProps({
  placeholder: {
    type: String,
    required: true
  },
})
</script>