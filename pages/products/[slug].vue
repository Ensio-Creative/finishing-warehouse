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
</script>

<template>
  <Head>
    <Title>{{ products[$route.params.slug].title }} - Finishing Warehouse </Title>
  </Head>
  <div>
    <HeroComp :img="$route.params.slug" />
    <div class="lg:px-20 py-10 px-4">
      <p class="lg:text-4xl mb-6 font-semibold text-3xl">{{ products[$route.params.slug].title }}</p>
      <div class="flex flex-wrap justify-between">
        <div class="mb-3 lg:w-[33%]" v-for="slide in 6" :key="slide">
          <img :src="'/images/products/1/img' + slide + '.png'" alt="">
          <p class="p-2 text-center text-lg">{{ products[$route.params.slug].title }}</p>
        </div>
      </div>
    </div>
  </div>
</template>