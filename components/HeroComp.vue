<script setup lang="ts">
defineProps<{
  img: string;
  text: string;
}>()
</script>

<template>
  <div class="relative mt-20">
    <img class="w-screen lg:h-[70vh] h-[60vh] object-cover" :src="'/images/hero/' + img + '.png'" />
    <div class="bg-[#0F0F0F33] absolute top-0 w-full lg:h-[70vh] h-[60vh] "></div>
    <p class="lg:text-4xl absolute bottom-10 lg:left-20 left-4 text-white font-medium mb-4 text-3xl">{{ text }}</p>
    <!-- <div class="bg-gradient-to-t from-[#FFFFFF00] from-50% to-[#FFFFFF] absolute top-0 w-full lg:h-[70vh] h-[60vh] "></div> -->
  </div>
</template>