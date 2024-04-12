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
    <div class="relative mt-20">
      <Carousel ref="myCarousel" :autoplay="6000" :wrap-around="true" :transition="600">
        <slide v-for="slide in 6" :key="slide">
          <div class="">
            <img class="w-screen object-cover lg:h-[90vh] h-[40vh]" :src="'/images/hero/slide-' + slide + '.png'"
              alt="">
          </div>
        </slide>
      </Carousel>
      <div class="bg-[#0F0F0F33] absolute top-0 w-full lg:h-[90vh] h-[40vh] ">
      </div>

      <div class="absolute lg:top-60 top-28 left-0 right-0 text-center">
        <p class="lg:text-5xl text-3xl text-white font-bold">Home for innovative and <br>
          eco-friendly bathroom <br>
          solutions</p>
      </div>
    </div>
    <!-- <video autoplay loop muted class="w-full lg:-mt-10 object-cover lg:h-[110vh] h-[80vh]">
      <source src="/images/hero-vid.mp4" type="video/mp4">
    </video> -->
    <div class="bg-[#F6F6F6] lg:py-32 px-6 py-16">
      <div class="lg:w-[70%] mx-auto text-center">
        <p class="lg:text-4xl mb-4 text-xl ">About Finishing Warehouse</p>
        <p class="text-[18px]">At Finishing Warehouse, we are committed to providing sustainable housing finishing
          solutions that not only
          enhance your space but also minimize our environmental footprint. From exquisite bathroom solutions to stylish
          kitchen fittings, ambient lighting, and elegant wall finishings, we offer eco-friendly materials and
          energy-efficient lighting products and services that prioritize sustainability without compromising on quality
          or style.
          <br> <br>
          Explore our wide range of products and discover how we can turn your vision into reality. Whether you're
          renovating your home or undertaking a large-scale construction project, trust Finishing Warehouse to deliver
          excellence every step of the way.
        </p>
        <NuxtLink to="/about">
          <button class="my-3 text-[#84240C] text-[18px]">LEARN MORE</button>
        </NuxtLink>
      </div>

    </div>
    <div class="lg:px-20 px-4 py-10">
      <div class="flex justify-between">
        <p class="lg:text-[40px] font-medium text-2xl">Products Categories</p>
      </div>
      <div class="lg:flex justify-between my-4">
        <div class="lg:w-[33%] lg:mb-0 mb-4 relative">
          <NuxtLink to="/products/1">
            <img class="w-full" src="/images/categories/001.png" alt="">
            <div class="bg-[#0F0F0F] flex justify-between p-5">
              <p class="lg:text-3xl text-2xl text-white ">Bathroom Finish</p>
              <img src="/images/icons/arrow-1.svg" alt="">
            </div>
          </NuxtLink>
        </div>
        <div class="lg:w-[33%] lg:mb-0 mb-4  relative">
          <NuxtLink to="/products/2">
            <img class="w-full" src="/images/categories/002.png" alt="">
            <div class="bg-[#0F0F0F] flex justify-between p-5">
              <p class=" lg:text-3xl text-2xl  text-white ">Wall Finish</p>
              <img src="/images/icons/arrow-1.svg" alt="">
            </div>
          </NuxtLink>
        </div>
        <div class="lg:w-[33%] lg:mb-0 mb-4  relative">
          <NuxtLink to="/products/3">
            <img class="w-full" src="/images/categories/003.png" alt="">
            <div class="bg-[#0F0F0F] flex justify-between p-5">
              <p class=" lg:text-3xl text-2xl text-white ">Kitchen Finish</p>
              <img src="/images/icons/arrow-1.svg" alt="">
            </div>
          </NuxtLink>
        </div>
      </div>
      <div class="text-center my-6">
        <NuxtLink to="/products">
          <button
            class="text-[18px] text-center  mx-auto text-[#84240C] lg:w-60 w-[70%] font-semibold p-2 my-auto">DISCOVER
            MORE
            <!-- <img class="my-auto"src="/images/arrow.svg" alt=""> -->
          </button>
        </NuxtLink>
      </div>
      <div class="pt-12 lg:flex">
        <div class="lg:w-1/2 lg:mb-0 mb-4"> <img class="lg:h-[100vh] object-cover w-full" src="/images/abt-1.png"
            alt="">
        </div>
        <div class="lg:w-1/2 lg:ml-3">
          <img class="lg:mb-3 mb-4 lg:h-[49vh] object-cover w-full " src="/images/abt-3.png" alt="">
          <img class=" lg:h-[49vh] object-cover w-full" src="/images/abt-2.png" alt="">
        </div>
        <!-- <img src="/images/quality-seal.png" class="absolute lg:w-auto w-20 lg:top-10 top-14 left-0 right-0 mx-auto"
          alt=""> -->
        <!-- <img src="/images/product-chair.png" class="lg:h-auto h-[209px] object-cover" alt=""> -->
      </div>

      <div class="pt-6">
        <div class="flex my-8 justify-between">
          <p class="lg:text-[40px] font-medium text-2xl">Projects</p>
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
          <div class="border-b lg:py-6 text-center my-6 vorder-[#7D7D7D]">
            <p class="lg:text-[40px] font-medium text-2xl lg:mb-0 mb-4">Brand Partners</p>
          </div>
          <div class="flex justify-between flex-wrap">
            <div class="mb-3 lg:w-[13%] w-[48%]" v-for="index in 7" :key="index">
              <img class="" :src="'/images/brands/00' + index + '.png'" alt="">
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
