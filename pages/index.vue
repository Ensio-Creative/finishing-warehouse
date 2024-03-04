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
    <div class="relative">
      <Carousel ref="myCarousel" :autoplay="6000" :wrap-around="true" :transition="600">
        <slide v-for="slide in 4" :key="slide">
          <div class="">
            <img class="w-screen object-cover lg:h-[100vh] h-[90vh]" :src="'/images/hero/slide-' + slide + '.png'" alt="">
          </div>
        </slide>
      </Carousel>
      <div class="bg-gradient-to-t from-[#FFFFFF00] from-40% to-[#FFFFFF] absolute top-0 w-full lg:h-[100vh] h-[90vh] ">
      </div>
      <div class="absolute lg:top-72 top-52 left-0 right-0 text-center">
        <p class="text-5xl text-white font-bold">Embrace the power of <br>
          quality and aesthetics</p>
      </div>
    </div>
    <!-- <video autoplay loop muted class="w-full lg:-mt-10 object-cover lg:h-[110vh] h-[80vh]">
      <source src="/images/hero-vid.mp4" type="video/mp4">
    </video> -->
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
          <NuxtLink to="/products/1">
            <img class="w-full" src="/images/categories/001.png" alt="">
            <p class="lg:text-3xl text-2xl absolute bottom-5 text-white left-5">Bathroom Finish</p>
          </NuxtLink>
        </div>
        <div class="lg:w-[33%] lg:mb-0 mb-4  relative">
          <NuxtLink to="/products/2">
            <img class="w-full" src="/images/categories/002.png" alt="">
            <p class=" lg:text-3xl text-2xl  absolute bottom-5 text-white left-5">Wall Finish</p>
          </NuxtLink>
        </div>
        <div class="lg:w-[33%] lg:mb-0 mb-4  relative">
          <NuxtLink to="/products/3">
            <img class="w-full" src="/images/categories/003.png" alt="">
            <p class=" lg:text-3xl text-2xl  absolute bottom-5 text-white left-5">Kitchen Finish</p>
          </NuxtLink>
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
        <img src="/images/product-chair.png" class="lg:h-auto h-[209px] object-cover" alt="">
      </div>

      <div class="pt-6">
        <div class="flex my-8 justify-between">
          <p class="lg:text-4xl font-semibold text-2xl">Projects</p>
          <div class="flex lg:w-28 w- justify-between">
            <img @click="myCarousel.prev()" class="w-12 cursor-pointer" src="/images/prev.svg" alt="">
            <img @click="myCarousel.next()" class="w-12 lg:ml-0 ml-2 cursor-pointer" src="/images/next.svg" alt="">
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
