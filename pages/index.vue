<script>
import { defineComponent } from 'vue'
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'

export default defineComponent({
  setup() {
    const myCarousel = ref(null)
    return {
      myCarousel
    }
  },
  components: {
    Carousel,
    Slide,
    Pagination,
    Navigation,
  },
})
</script>

<template>
  <Head>
    <Title>Finishing Warehouse - </Title>
  </Head>
  <div>
    <video autoplay loop muted class="w-full lg:-mt-10 object-cover lg:h-[110vh] h-[80vh]">
      <source src="/images/hero-vid.mp4" type="video/mp4">
    </video>
    <div class="bg-[#F6F6F6] lg:p-20 p-6">
      <p class="lg:text-2xl text-xl lg:w-1/2 mx-auto text-center">Discover the perfect blend of glamour and quality with
        endless rides
        of appealing experiences for your building
        and spaces.</p>
    </div>
    <div class="lg:px-20 px-4 py-10">
      <div class="flex justify-between">
        <p class="lg:text-4xl text-2xl">Products Categories</p>
        <NuxtLink to="/products">
          <button class="border border-[#0F0F0F] text-sm p-2 my-auto">DISCOVER MORE</button>
        </NuxtLink>
      </div>
      <div class="lg:flex justify-between my-4">
        <div class="lg:w-[32%] lg:mb-0 mb-4 relative">
          <img class="w-full" src="/images/categories/001.png" alt="">
          <p class="lg:text-2xl text-lg absolute bottom-5 text-white left-5">Bathroom Finish</p>
        </div>
        <div class="lg:w-[32%] lg:mb-0 mb-4  relative">
          <img class="w-full" src="/images/categories/002.png" alt="">
          <p class="text-2xl lg:text-2xl text-lg  absolute bottom-5 text-white left-5">Wall Finish</p>
        </div>
        <div class="lg:w-[32%] lg:mb-0 mb-4  relative">
          <img class="w-full" src="/images/categories/003.png" alt="">
          <p class="text-2xl lg:text-2xl text-lg  absolute bottom-5 text-white left-5">Kitchen Finish</p>
        </div>
      </div>
      <div class="pt-24 relative">
        <img src="/images/quality-seal.png" class="absolute lg:w-auto w-20 lg:top-10 top-14 left-0 right-0 mx-auto"
          alt="">
        <img src="/images/about.png" class="" alt="">
      </div>

      <div class="pt-6">
        <div class="flex my-8 justify-between">
          <p class="lg:text-4xl text-2xl">Projects</p>
          <div class="flex w-28 justify-between">
            <img @click="myCarousel.prev()" class="w-12 cursor-pointer" src="/images/prev.png" alt="">
            <img @click="myCarousel.next()" class="w-12 cursor-pointer" src="/images/next.png" alt="">
          </div>
        </div>
        <Carousel ref="myCarousel" :items-to-show="1.8" :wrapAround="true">
          <slide v-for="slide in 3" :key="slide">
            <div class="mr-6">
              <img class="w-full" :src="'/images/projects/projects' + slide + '.png'" alt="">
            </div>
          </slide>
        </Carousel>
      </div>
      <div class="pt-6">
        <div class="lg:flex my-8 justify-between">
          <p class="lg:text-4xl text-2xl lg:mb-0 mb-4">Brand Partners</p>
          <div class="lg:w-[53%] flex justify-between flex-wrap">
            <div class="mb-3 lg:w-[32%] w-[48%]" v-for="index in 6" :key="index">
              <img class="" :src="'/images/brands/00' + index + '.png'" alt="">
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
