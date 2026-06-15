<template>
  <NuxtLoadingIndicator />
  <div class="app">
    <HeaderNav />
    <NuxtPage :key="$route.fullPath" />
    <FooterNav />
  </div>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Manrope:wght@200..800&display=swap');

.app {
  font-family: "Manrope", sans-serif;
}
</style>