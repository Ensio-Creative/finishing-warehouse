<script setup>
const slider = ref([
  "",
  "Bathroom Finish",
  "Wall Finish",
  "Kitchen Finish",
  "Indoor Finish",
  "Outdoor Finish",
  "Home Decor",
  "Lighting ",
  "Curtains"
])
</script>

<template>
  <Head>
    <Title>Products - Finishing Warehouse </Title>
  </Head>
  <div>
    <HeroComp img="products" />
    <div class="lg:px-20 px-4 py-10">
      <p class="lg:text-4xl text-3xl font-semibold">Product Categories</p>
      <!-- <p>Explore our product categories.</p> -->


      <div v-for="slide in 8" :key="slide" class="my-6 relative">
        <NuxtLink :to="'/products/' + slide">
          <img class=" lg:h-auto h-72" :src="'/images/products/product' + slide + '.png'" alt="">
          <p class="absolute bottom-6 lg:left-10 left-4 lg:text-4xl text-2xl text-white">{{ slider[slide] }}</p>
        </NuxtLink>
      </div>
      <!-- <div class="my-6 relative">
        <img class=" lg:h-auto h-72" src="/images/products/product2.png" alt="">
        <p class="absolute bottom-6 lg:left-10 left-4 lg:text-4xl text-2xl text-white">Wall Finish</p>
      </div>
      <div class="my-6 relative">
        <img class=" lg:h-auto h-72" src="/images/products/product3.png" alt="">
        <p class="absolute bottom-6 lg:left-10 left-4 lg:text-4xl text-2xl text-white">Kitchen Finish</p>
      </div>
      <div class="my-6 relative">
        <img class=" lg:h-auto h-72" src="/images/products/product4.png" alt="">
        <p class="absolute bottom-6 lg:left-10 left-4 lg:text-4xl text-2xl text-white">Indoor Finish</p>
      </div>
      <div class="my-6 relative">
        <img class=" lg:h-auto h-72" src="/images/products/product5.png" alt="">
        <p class="absolute bottom-6 lg:left-10 left-4 lg:text-4xl text-2xl text-white">Outdoor Finish</p>
      </div>
      <div class="my-6 relative">
        <img class=" lg:h-auto h-72" src="/images/products/product6.png" alt="">
        <p class="absolute bottom-6 lg:left-10 left-4 lg:text-4xl text-2xl text-white">Home Decor</p>
      </div>
      <div class="my-6 relative">
        <img class=" lg:h-auto h-72" src="/images/products/product7.png" alt="">
        <p class="absolute bottom-6 lg:left-10 left-4 lg:text-4xl text-2xl text-white">Lighting</p>
      </div>
      <div class="my-6 relative">
        <img class=" lg:h-auto h-72" src="/images/products/product8.png" alt="">
        <p class="absolute bottom-6 lg:left-10 left-4 lg:text-4xl text-2xl text-white">Curtains</p>
      </div> -->
    </div>
  </div>
</template>