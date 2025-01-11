<template>
    <div class="relative w-full text-black">
        <label>{{ label }}</label>
        <input
            type="date"
            class="w-[97%] border-[1px] bg-white p-2 focus:outline-none rounded mt-3"
        >
  </div>
</template>

<script setup lang="ts">
   import {defineProps} from "vue";
   defineProps({
    label:{
        required: true,
        type: String,
    }
   })
</script>


