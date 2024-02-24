<script>
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide } from 'vue3-carousel'

export default {
  data() {
    return {
      slider: [
        "",
        "Bathroom Finish",
        "Wall Finish",
        "Kitchen Finish",
        "Indoor Finish",
        "Outdoor Finish",
        "Home Decor",
        "Lighting",
        "Curtains"
      ]
    }
  },
  components: {
    Carousel,
    Slide
  },
}
</script>

<template>
  <div class="my-6">
    <carousel :items-to-show="3.5">
      <slide v-for="slide in 8" :key="slide">
        <div class="relative">
          <img :src="'/images/products/' + slide + '.png'" class="object-cover w-full h-80" alt="">
          <div class="-rotate-90 text-base absolute text-white bottom-14 text-left -right-6">{{ slider[slide] }}</div>
          <img class="absolute top-3 right-3 w-6" src="/images/icons/arrow.png" alt="">
        </div>
      </slide>
    </carousel>
  </div>
</template>