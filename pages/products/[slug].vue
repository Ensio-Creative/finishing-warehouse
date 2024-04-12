<script setup>
const products = ref([
  {},
  {
    title: "Bathroom Finish",
  }, {
    title: "Wall Finish"
  }, {
    title: "Kitchen Finish"
  }, {
    title: "Indoor Finish"
  }, {
    title: "Outdoor Finish"
  }, {
    title: "Home Decor"
  }, {
    title: "Lighting"
  }, {
    title: "Curtains"
  }
])

const product1 = ref([
  "Closed Coupled WCs",
  "Concealed / Hung WCs",
  "Mirrors",
  "Vanities Wash Basins",
  "Wash Basins",
  "Showers",
  "Shower Channels | Drains",
  "Bathroom Essentials"
])
</script>

<template>

  <Head>
    <Title>{{ products[$route.params.slug].title }} - Finishing Warehouse </Title>
  </Head>
  <div>
    <HeroComp :img="$route.params.slug" :text="products[$route.params.slug].title" />
    <div class="lg:px-20 py-10 px-4">
      <!-- <p class="lg:text-4xl mb-6 font-semibold text-3xl">{{ products[$route.params.slug].title }}</p> -->
      <div class="flex flex-wrap justify-between">
        <div class="mb-3 lg:w-[33%]" v-for="slide in 8" :key="slide">
          <img :src="'/images/products/2/img' + slide + '.png'" alt="">
          <p class="p-2 text-center text-lg">{{ product1[slide-1] }}</p>
        </div>
        <div class="lg:w-[33%]"></div>
      </div>
    </div>
  </div>
</template>