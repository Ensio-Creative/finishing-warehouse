<script setup lang="ts">
const position = ref(0)
const toggle = ref(false)
const products = ref(false)
const dropdown = ref(false)
onMounted(() => {
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
  <div
    class="w-full bg-[#FFFFFF] flex justify-between lg:px-20 px-4 py-5">
    <NuxtLink @click="dropdown = false" to="/" class="z-30">
      <img class="lg:w-auto w-[140px] my-auto" src="/images/logo.png" />
    </NuxtLink>
    <img @click="toggle = !toggle" class="lg:hidden block cursor-pointer" src="/images/icons/bars.svg" alt="">
    <div class="w-[40%] z-10 uppercase lg:flex hidden justify-between my-auto text-sm">
      <NuxtLink to="/">
        <p>Home</p>
      </NuxtLink>
      <p class="flex cursor-pointer">
        <NuxtLink to="/products">
          Products
        </NuxtLink>
        <img v-if="dropdown" @click="dropdown = !dropdown" class="my-auto ml-2" src="/images/icons/more.svg" alt="">
        <img v-else @click="dropdown = !dropdown" class="my-auto rotate-180 ml-2" src="/images/icons/more.svg" alt="">
      </p>
      <NuxtLink to="/projects">
        <p>Projects</p>
      </NuxtLink>
      <NuxtLink to="/about">
        <p>About us</p>
      </NuxtLink>
      <NuxtLink to="/contact">
        <p>Contact</p>
      </NuxtLink>
    </div>
    <div v-show="dropdown" class="w-full bg-white absolute top-0 left-0 h-screen">
      <div class="flex px-20 py-32">
        <div class="w-[12.5%] relative">
          <NuxtLink to="/products/1" @click="dropdown = !dropdown">
            <img src="/images/products/1.png" class="object-cover w-full h-80" alt="">
            <div class="-rotate-90 text-xl absolute text-white bottom-20 -right-12">Bathroom Finish</div>
            <img class="absolute top-3 cursor-pointer right-3 w-6" src="/images/icons/arrow.svg" alt="">
          </NuxtLink>
        </div>
        <div class="w-[12.5%] relative">
          <NuxtLink to="/products/2" @click="dropdown = !dropdown">
            <img src="/images/products/2.png" class="object-cover w-full h-80" alt="">
            <div class="-rotate-90 text-xl absolute text-white bottom-14 -right-6">Wall Finish</div>
            <img class="absolute top-3 cursor-pointer right-3 w-6" src="/images/icons/arrow.svg" alt="">
          </NuxtLink>
        </div>
        <div class="w-[12.5%] relative">
          <NuxtLink to="/products/3" @click="dropdown = !dropdown">
            <img src="/images/products/3.png" class="object-cover h-80 w-full" alt="">
            <div class="-rotate-90 text-xl absolute text-white bottom-16 -right-11">Kitchen Finish</div>
            <img class="absolute top-3 cursor-pointer right-3 w-6" src="/images/icons/arrow.svg" alt="">
          </NuxtLink>
        </div>
        <div class="w-[12.5%] relative">
          <NuxtLink to="/products/4" @click="dropdown = !dropdown">
            <img src="/images/products/4.png" class="object-cover w-full h-80" alt="">
            <div class="-rotate-90 text-xl absolute text-white bottom-16 -right-10">Indoor Finish</div>
            <img class="absolute top-3 cursor-pointer right-3 w-6" src="/images/icons/arrow.svg" alt="">
          </NuxtLink>
        </div>
        <div class="w-[12.5%] relative">
          <NuxtLink to="/products/5" @click="dropdown = !dropdown">
            <img src="/images/products/5.png" class="object-cover h-80 w-full" alt="">
            <div class="-rotate-90 text-xl absolute text-white bottom-20 -right-12">Outdoor Finish</div>
            <img class="absolute top-3 cursor-pointer right-3 w-6" src="/images/icons/arrow.svg" alt="">
          </NuxtLink>
        </div>
        <div class="w-[12.5%] relative">
          <NuxtLink to="/products/6" @click="dropdown = !dropdown">
            <img src="/images/products/6.png" class="object-cover h-80 w-full" alt="">
            <div class="-rotate-90 text-xl absolute text-white bottom-16 -right-8">Home Decor</div>
            <img class="absolute top-3 cursor-pointer right-3 w-6" src="/images/icons/arrow.svg" alt="">
          </NuxtLink>
        </div>
        <div class="w-[12.5%] relative">
          <NuxtLink to="/products/7" @click="dropdown = !dropdown">
            <img src="/images/products/7.png" class="object-cover h-80 w-full" alt="">
            <div class="-rotate-90 text-xl absolute text-white bottom-12 -right-4">Lighting</div>
            <!-- <div class="-rotate-90 text-xl absolute text-white bottom-16 -right-8">Home Decor</div> -->
            <img class="absolute top-3 cursor-pointer right-3 w-6" src="/images/icons/arrow.svg" alt="">
          </NuxtLink>
        </div>
        <div class="w-[12.5%] relative">
          <NuxtLink to="/products/8" @click="dropdown = !dropdown">
            <img src="/images/products/8.png" class="object-cover h-80 w-full" alt="">
            <div class="-rotate-90 text-xl absolute text-white bottom-12 -right-4">Curtains</div>
            <!-- <div class="-rotate-90 text-xl absolute text-white bottom-16 -right-8">Home Decor</div> -->
            <img class="absolute top-3 cursor-pointer right-3 w-6" src="/images/icons/arrow.svg" alt="">
          </NuxtLink>
        </div>
      </div>
    </div>
    <div v-if="toggle" class="fixed top-0 left-0 w-full p-6 h-screen bg-white">
      <img @click="toggle = false" class="ml-auto cursor-pointer" src="/images/icons/close.svg" alt="">
      <div class="border-b my-4 mt-8  border-[#D9D9D9]">
        <NuxtLink to="/" @click="toggle = !toggle">
          <p class="text-3xl py-3">Home</p>
        </NuxtLink>
      </div>
      <div class="border-b py-3 flex flex-wrap justify-between my-4 border-[#D9D9D9]">
        <NuxtLink to="/products" @click="toggle = !toggle">
          <p class="text-3xl ">Products</p>
        </NuxtLink>
        <img v-if="products === false" @click="products = !products" class="w-6 cursor-pointer"
          src="/images/icons/plus.svg" alt="">
        <img v-else class="w-6 cursor-pointer" @click="products = !products" src="/images/icons/hide.svg" alt="">

        <div class="w-full" v-show="products">
          <MobileProducts :toggle="setToggle" />
        </div>
      </div>
      <div class="border-b my-4 border-[#D9D9D9]">
        <NuxtLink to="/projects" @click="toggle = !toggle">
          <p class="text-3xl py-3">Projects</p>
        </NuxtLink>
      </div>
      <div class="border-b my-4 border-[#D9D9D9]">
        <NuxtLink to="/about" @click="toggle = !toggle">
          <p class="text-3xl py-3">About us</p>
        </NuxtLink>
      </div>
      <div class="border-b my-4 border-[#D9D9D9]">
        <NuxtLink to="/contact" @click="toggle = !toggle">
          <p class="text-3xl py-3">Contact</p>
        </NuxtLink>
      </div>
    </div>
  </div>
</template>