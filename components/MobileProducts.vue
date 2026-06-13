<script>
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide } from 'vue3-carousel'

export default {
  data() {
    return {
      slider: [
        "",
        "WCs",
        "Washbasins",
        "Taps & Mixers",
        "Showers",
        "Assessories",
      ]
    }
  },
  components: {
    Carousel,
    Slide
  },
  props: {
    toggle: Function
  }
}
</script>

<template>
  <div class="my-6">
    <div v-for="slide in 8" :key="slide">
      <NuxtLink :to="'/products/' + slide" @click="toggle">
        <div class="text-xl my-3">{{
          slider[slide] }}</div>
      </NuxtLink>
    </div>

    <!-- <carousel :items-to-show="3.5">
      <slide v-for="slide in 8" :key="slide">
        <div class="relative">
          <img :src="'/images/products/' + slide + '.png'" class="object-cover w-full h-80" alt="">
          <NuxtLink :to="'/products/' + slide" @click="toggle">
            <img class="absolute top-3 right-3 cursor-pointer w-6" src="/images/icons/arrow.png" alt="">
          </NuxtLink>
        </div>
      </slide>
    </carousel> -->
  </div>
</template>