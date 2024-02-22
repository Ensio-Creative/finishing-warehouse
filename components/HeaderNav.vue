<script setup lang="ts">
const position = ref(false)


// setInterval(function () {
//   position.value = window?.scrollY
//   console.log(position)
// }, 5000);

</script>

<template>
  <div :class="position ? 'fixed z-10 top-0 w-full bg-white flex justify-between px-20 py-4' : 'fixed z-10 top-0 w-full flex justify-between px-20 py-4'">
    <img src="/images/finishing-warehouse-logo.png" />
    <div class="w-[35%] flex justify-between my-auto text-lg">
      <p>Home</p>
      <p>Products</p>
      <p>Projects</p>
      <p>About us</p>
      <p>Contact</p>
    </div>
  </div>
</template>