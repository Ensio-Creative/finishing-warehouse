<script setup>
const products = ref([
  {
    title: "Bathroom Finish",
    products: [
      "Closed Coupled WCs",
      "Concealed / Hung WCs",
      "Mirrors",
      "Vanities Wash Basins",
      "Wash Basins",
      "Showers",
      "Shower Channels | Drains",
      "Bathroom Essentials"
    ],
    slug: "bathroom-finish"
  }, {
    title: "Wall Finish",
    products: [],
    slug: ""
  }, {
    title: "Kitchen Finish",
    products: [],
    slug: ""
  }, {
    title: "Outdoor Finish",
    products: [],
    slug: ""
  }, {
    title: "Home Decor",
    products: [],
    slug: ""
  }, {
    title: "Lighting",
    products: [],
    slug: ""
  }, {
    title: "Curtains",
    products: [],
    slug: ""
  }
])

// onMounted(() => {
//   console.log(route.params.slug)
//   products.map(single => single.slug === $route.params.slug ? active.value = single : null)
// })

</script>

<template>

  <Head>
    <Title>{{ products[0].title }} - Finishing Warehouse </Title>
  </Head>
  <div>
    <HeroComp :img="1" :text="products[0].title" />
    <div class="lg:px-20 lg:py-20 py-12 px-4">
      <!-- <p class="lg:text-4xl mb-6 font-semibold text-3xl">{{ products[$route.params.slug].title }}</p> -->
      <div class="flex flex-wrap justify-between">
        <div class="mb-5 lg:w-[33%]" v-for="slide in 8" :key="slide">
          <img :src="'/images/products/2/img' + slide + '.png'" alt="">
          <p class="p-2 text-center text-[16px] text-[#0F0F0F] font-medium">{{ products[0].products[slide - 1] }}</p>
        </div>
        <div class="lg:w-[33%]"></div>
      </div>
    </div>
  </div>
</template>