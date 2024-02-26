
<script setup lang="ts">
defineProps<{
  img: string
}>()
</script>

<template>
  <div class="relative">
    <img class="w-screen lg:h-[80vh] h-[70vh] object-cover" :src="'/images/hero/' + img + '.png'" />
    <div class="bg-gradient-to-b from-[#FFFFFF00] to-[#FFFFFF] absolute top-0 w-full lg:h-[80vh] h-[70vh] "></div>
  </div>
</template>