<script setup lang="ts">

const position = ref(0)
const toggle = ref(false)
const products = ref(false)
const dropdown = ref(false)
const productCategories = [
  { name: 'WCs', slug: 'wcs' },
  { name: 'Washbasins', slug: 'washbasins' },
  { name: 'Taps & Mixers', slug: 'taps-mixers' },
  { name: 'Showers', slug: 'showers' },
  { name: 'Assessories', slug: 'assessories' }
]
const scrollToTop = () => {
  window.scrollTo({ top: 0, behavior: 'smooth' });
};

onMounted(() => {
  scrollToTop();

  setInterval(function () {
    position.value = window?.scrollY
    // console.log(window?.scrollY)
  }, 1000);
})


const setToggle = () => {
  toggle.value = !toggle
}
</script>

<template>
  <div class="w-full fixed top-0 z-30 bg-[#FFFFFF] flex justify-between lg:px-20 px-4 py-5">
    <NuxtLink @click="dropdown = false, scrollToTop()" to="/" class="z-30">
      <img class="lg:w-auto w-[140px] my-auto" src="/images/logo.png" />
    </NuxtLink>
    <img @click="toggle = !toggle" class="lg:hidden block cursor-pointer" src="/images/icons/bars.svg" alt="">
    <div class="w-[40%] z-10 uppercase text-[#0F0F0F] lg:flex hidden justify-between my-auto font-medium text-[12px]">
      <NuxtLink to="/" @click="scrollToTop()">
        <p @click="dropdown = false">Home</p>
      </NuxtLink>
      <div class="relative group" @mouseenter="dropdown = true" @mouseleave="dropdown = false">
        <p class="flex cursor-pointer">
          <NuxtLink to="/products">
            Products
          </NuxtLink>
          <img v-if="dropdown" class="my-auto ml-2" src="/images/caret-down-2.svg" alt="">
          <img v-else class="my-auto ml-2" src="/images/caret-down-1.svg" alt="">
        </p>
        <div v-if="dropdown" class="absolute top-full left-0 bg-white shadow-lg py-2 min-w-[200px] z-40">
          <NuxtLink v-for="cat in productCategories" :key="cat.slug" :to="`/products/${cat.slug}`" class="block px-4 capitalize py-2 hover:bg-gray-100" @click="dropdown = false">
            {{ cat.name }}
          </NuxtLink>
        </div>
      </div>
      <NuxtLink to="/services" @click="scrollToTop()">
        <p @click="dropdown = false">Services</p>
      </NuxtLink>
      <NuxtLink to="/projects">
        <p @click="dropdown = false">Projects</p>
      </NuxtLink>
      <NuxtLink to="/about">
        <p @click="dropdown = false">About us</p>
      </NuxtLink>
      <NuxtLink to="/contact">
        <p @click="dropdown = false">Contact</p>
      </NuxtLink>
    </div>

    <div v-if="toggle" class="fixed text-[#0F0F0F] top-0 left-0 w-full p-6 h-screen bg-white">
      <img @click="toggle = false" class="ml-auto mt-2 cursor-pointer" src="/images/close.svg" alt="">
      <div class="border-b my-4 mt-20  border-[#D9D9D9]">
        <NuxtLink to="/" @click="toggle = !toggle, scrollToTop()">
          <p class="text-2xl py-3 uppercase">Home</p>
        </NuxtLink>
      </div>

      <div class="border-b py-3 flex flex-wrap justify-between my-4 border-[#D9D9D9]">
        <NuxtLink to="/products" @click="toggle = !toggle">
          <p class="text-2xl uppercase">Products</p>
        </NuxtLink>
        <img v-if="products === false" @click="products = !products" class="w-6 cursor-pointer"
          src="/images/caret-down-2.svg" alt="">
        <img v-else class="w-6 cursor-pointer" @click="products = !products" src="/images/caret-down-1.svg" alt="">

        <div class="w-full" v-show="products">
          <div v-for="cat in productCategories" :key="cat.slug">
            <NuxtLink :to="`/products/${cat.slug}`" @click="toggle = false, products = false">
              <p class="text-lg uppercase py-3 pl-4">{{ cat.name }}</p>
            </NuxtLink>
          </div>
        </div>
      </div>
      <div class="border-b my-4  border-[#D9D9D9]">
        <NuxtLink to="/services" @click="toggle = !toggle, scrollToTop()">
          <p class="text-2xl uppercase py-3">Services</p>
        </NuxtLink>
      </div>
      <div class="border-b my-4 border-[#D9D9D9]">
        <NuxtLink to="/projects" @click="toggle = !toggle">
          <p class="text-2xl uppercase py-3">Projects</p>
        </NuxtLink>
      </div>
      <div class="border-b my-4 border-[#D9D9D9]">
        <NuxtLink to="/about" @click="toggle = !toggle">
          <p class="text-2xl uppercase py-3">About us</p>
        </NuxtLink>
      </div>
      <div class="border-b my-4 border-[#D9D9D9]">
        <NuxtLink to="/contact" @click="toggle = !toggle">
          <p class="text-2xl uppercase py-3">Contact</p>
        </NuxtLink>
      </div>

      <button class="uppercase text-sm text-white p-3 w-full mt-20 bg-[#84240C]">Get in Touch</button>
    </div>
  </div>
</template>