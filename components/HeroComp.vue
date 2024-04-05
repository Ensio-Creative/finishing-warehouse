
<script setup lang="ts">
defineProps<{
  img: string
}>()
</script>

<template>
  <div class="relative">
    <img class="w-screen lg:h-[60vh] h-[50vh] object-cover" :src="'/images/hero/' + img + '.png'" />
    <!-- <div class="bg-gradient-to-t from-[#FFFFFF00] from-50% to-[#FFFFFF] absolute top-0 w-full lg:h-[70vh] h-[60vh] "></div> -->
  </div>
</template>