<script>
import { defineComponent } from 'vue'
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'

export default defineComponent({
  setup() {
    const myCarousel = ref(null)
    return {
      myCarousel,
      breakpoints: {
        // 700px and up
        700: {
          itemsToShow: 1,
          // snapAlign: "center"
        },
        // 1024 and up
        1024: {
          itemsToShow: 1.7,
          // snapAlign: "start"
        }
      }
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
    <div class="bg-[#F6F6F6] lg:h-[400px] lg:py-32 px-6 py-16">
      <p class="lg:text-4xl text-xl lg:w-[60%] mx-auto text-center">Discover the perfect blend of glamour and quality with
        endless rides
        of appealing experiences for your building
        and spaces.</p>
    </div>
    <div class="lg:px-20 px-4 py-10">
      <div class="flex justify-between">
        <p class="lg:text-4xl font-semibold text-2xl">Products Categories</p>
      </div>
      <div class="lg:flex justify-between my-4">
        <div class="lg:w-[33%] lg:mb-0 mb-4 relative">
          <img class="w-full" src="/images/categories/001.png" alt="">
          <p class="lg:text-3xl text-3xl absolute bottom-5 text-white left-5">Bathroom Finish</p>
        </div>
        <div class="lg:w-[33%] lg:mb-0 mb-4  relative">
          <img class="w-full" src="/images/categories/002.png" alt="">
          <p class=" lg:text-3xl text-3xl  absolute bottom-5 text-white left-5">Wall Finish</p>
        </div>
        <div class="lg:w-[33%] lg:mb-0 mb-4  relative">
          <img class="w-full" src="/images/categories/003.png" alt="">
          <p class=" lg:text-3xl text-3xl  absolute bottom-5 text-white left-5">Kitchen Finish</p>
        </div>
      </div>
      <div class="text-center">
        <NuxtLink to="/products">
          <button class="border-2 border-[#0F0F0F] text-sm lg:w-52 w-full font-semibold p-2 my-auto">DISCOVER
            MORE</button>
        </NuxtLink>
      </div>
      <div class="pt-12 relative">
        <!-- <img src="/images/quality-seal.png" class="absolute lg:w-auto w-20 lg:top-10 top-14 left-0 right-0 mx-auto"
          alt=""> -->
        <img src="/images/about.png" class="" alt="">
      </div>

      <div class="pt-6">
        <div class="flex my-8 justify-between">
          <p class="lg:text-4xl font-semibold text-2xl">Projects</p>
          <div class="flex w-28 justify-between">
            <img @click="myCarousel.prev()" class="w-12 cursor-pointer" src="/images/prev.png" alt="">
            <img @click="myCarousel.next()" class="w-12 cursor-pointer" src="/images/next.png" alt="">
          </div>
        </div>
        <Carousel ref="myCarousel" :breakpoints="breakpoints">
          <slide v-for="slide in 3" :key="slide">
            <div class="mr-2">
              <img class="w-full" :src="'/images/projects/projects' + slide + '.png'" alt="">
            </div>
          </slide>
        </Carousel>
      </div>
      <div class="pt-6">
        <div class="mt-8">
          <div class="border-b lg:py-6 my-6 vorder-[#7D7D7D]">
            <p class="lg:text-4xl font-semibold text-2xl lg:mb-0 mb-4">Brand Partners</p>
          </div>
          <div class="flex justify-between flex-wrap">
            <div class="mb-3 lg:w-[15%] w-[48%]" v-for="index in 6" :key="index">
              <img class="" :src="'/images/brands/00' + index + '.png'" alt="">
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
