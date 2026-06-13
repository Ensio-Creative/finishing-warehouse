<script setup>
const slider = ref([
  "WCs",
  "Washbasins",
  "Taps & Mixers",
  "Showers",
  "Assessories"
])
const slugify = (s) => s.toLowerCase().replace(/[^a-z0-9]+/g, '-').replace(/(^-|-$)/g, '')
</script>

<template>

  <Head>
    <Title>Products - Finishing Warehouse </Title>
  </Head>
  <div>
    <HeroComp img="products" text="Products" />
    <div class="lg:px-20 px-4 lg:py-20 py-8">
      <div class="grid lg:grid-cols-2 gap-4">
        <NuxtLink v-for="(item, index) in slider" :key="index" :to="`/products/${slugify(item)}`" class="block" :class="`relative ${index === 2 && 'lg:col-span-2'}`">
          <img :src="`/images/products/product-${index+1}.jpg`" :alt="item" class="w-full lg:h-full h-[35vh] object-cover">
          <div class="bg-[#0F0F0F]/60 absolute top-0 w-full lg:h-full h-[35vh] "></div>
          <p class="text-white absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 p-4 text-center text-xl">{{ item }}</p>
        </NuxtLink>
      </div>
    </div>
  </div>
</template>