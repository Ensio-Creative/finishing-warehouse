<script setup>
const products = ref([
  {
    title: "WCs",
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
    slug: "wcs"
  }, {
    title: "Washbasins",
    products: [],
    slug: "washbasins"
  }, {
    title: "Taps & Mixers",
    products: [],
    slug: "taps-mixers"
  }, {
    title: "Showers",
    products: [],
    slug: "showers"
  }, {
    title: "Assessories",
    products: [],
    slug: "assessories"
  }
])

const route = useRoute()
const activeCategory = computed(() => products.value.find(p => p.slug === route.params.slug) || null)
</script>

<template>
  <Head>
    <title>{{ activeCategory?.title || 'Products' }} - Finishing Warehouse</title>
  </Head>
  <div v-if="activeCategory">
    <HeroComp :img="1" :text="activeCategory.title" />
    <div class="lg:px-20 lg:py-20 py-12 px-4">
      <p class="lg:text-4xl mb-6 font-semibold text-3xl">{{ activeCategory.title }}</p>
      <div class="flex flex-wrap justify-between">
        <div class="mb-5 lg:w-[33%]" v-for="(product, idx) in activeCategory.products" :key="idx">
          <img :src="'/images/products/2/img' + (idx + 1) + '.png'" alt="">
          <p class="p-2 text-center text-[16px] text-[#0F0F0F] font-medium">{{ product }}</p>
        </div>
        <div class="lg:w-[33%]" v-if="!activeCategory.products.length">
          <p>No products available for this category yet.</p>
        </div>
      </div>
    </div>
  </div>
</template>