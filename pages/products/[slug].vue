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
      <p class="lg:text-4xl text-2xl">{{ products[$route.params.slug].title }}</p>
    </div>
  </div>
</template>