<script>
import { defineComponent, ref, reactive } from 'vue'
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'



export default defineComponent({
  setup() {
    const myCarousel = ref(null);
    const data = reactive([
      {
        title: "We Set Trends",
        text: "Our offerings are inspired by global styles and tailored for the Nigerian market."
      },
      {
        title: "We Ensure Quality",
        text: "Partnering with trusted international and local brands, we deliver only the best materials and products."
      },
      {
        title: "We Focus on You",
        text: "Personalized consultations and bespoke solutions ensure that every client’s needs are met."
      },
      {
        title: "We Transform Spaces",
        text: "Beyond products, we deliver a lifestyle upgrade that makes every home stand out."
      }
    ]);
    return {
      myCarousel,
      data,
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
    <Title>Finishing Warehouse - Home for innovative and eco-friendly finishing solutions</Title>
  </Head>
  <div>
    <div class="relative mt-20">
      <Carousel ref="myCarousel" :autoplay="6000" :wrap-around="true" :transition="600">
        <slide v-for="slide in 3" :key="slide">
          <div class="">
            <img class="w-screen object-cover lg:h-[90vh] h-[70vh]" :src="'/images/hero/slide' + slide + '.jpg'" alt="">
          </div>
        </slide>
      </Carousel>
      <div class="bg-[#0F0F0F]/60 absolute top-0 w-full lg:h-[90vh] h-[70vh] ">
      </div>

      <div class="absolute lg:top-60 top-60 lg:left-0 lg:right-0 left-4 right-4 text-center">
        <div class="lg:w-[55%] mx-auto">
          <p class="lg:text-[18px] mb-6 text-base text-white">Finishing Warehouse Nigeria Limited</p>
          <p class="lg:text-[50px] lg:leading-[50px] text-3xl text-white font-bold">Transforming Bathrooms and
            Kitchens into Lifestyle Statements</p>
        </div>
      </div>

      <!-- <div
        class="absolute flex justify-center right-0 left-0 lg:mx-auto mx-4 lg:w-[35%] text-[#84240C] p-4 lg:gap-10 gap-5 lg:top-[540px] top-[300px] bg-white rounded-md">
        <p class="lg:text-base text-sm">BATHROOMS</p>
        <div class="border-r border-[#D9D9D9]"></div>
        <p class="lg:text-base text-sm">KITCHENS</p>
        <div class="border-r border-[#D9D9D9]"></div>
        <p class="lg:text-base text-sm">LIFESTYLES</p>
      </div> -->
    </div>

    <div class="lg:px-20 px-4 lg:py-20 py-16">
      <div class="flex justify-between">
        <div class="lg:w-[50%]">
          <p class="lg:text-[35px] font-medium text-[#84240C] lg:mb-6 mb-4 text-2xl">Where every product makes
            a statement </p>
        </div>
        <NuxtLink to="/products" class="my-auto">
          <button
            class="uppercase lg:block hidden my-auto bg-[#84240C] text-white rounded-full px-10 py-2 text-sm">Discover
            All
            Products</button>
        </NuxtLink>

      </div>
      <div class="grid lg:grid-cols-3 gap-4 my-4">
        <div>
          <img src="/images/products/Home-WCs.jpg" alt="">
          <NuxtLink to="/products/wcs">
            <p class="my-4 underline">WCs</p>
          </NuxtLink>
        </div>
        <div>
          <img src="/images/products/Home-Washbasins.jpg" alt="">
          <NuxtLink to="/products/washbasins">
            <p class="my-4 underline">Washbasins</p>
          </NuxtLink>
        </div>
        <div>
          <img src="/images/products/Home-Taps-&-Mixers.jpg" alt="">
          <NuxtLink to="/products/taps-mixers">
            <p class="my-4 underline">Taps & Mixers</p>
          </NuxtLink>
        </div>
      </div>

      <div class="text-center">
        <NuxtLink to="/products">
          <button
            class="uppercase lg:hidden mx-auto block lg:my-auto my-8 bg-[#84240C] text-white rounded-full w-full px-10 py-3 text-sm">Discover
            All
            Products
          </button>
        </NuxtLink>
      </div>
    </div>
    <div class="relative">
      <img src="/images/New-Showers.jpg" class="lg:h-[700px] w-full object-cover h-[60vh] " alt="">
      <div class="bg-[#0F0F0F]/60 absolute top-0 w-full lg:h-[700px] h-[60vh] ">
      </div>
      <div
        class="absolute lg:text-left text-white lg:left-20 lg:p-0 p-4 lg:top-96 lg:mt-0 mt-20 top-24 bottom-0 lg:w-[475px]">
        <p class="text-sm mb-6">Our Commitment</p>
        <p class="lg:text-[35px] text-2xl leading-tight">To provide sustainable finishing solutions that enhance your space and improve your
          quality of life.</p>
      </div>
    </div>

    <div class="lg:px-20 px-4 lg:py-20 py-8">
      <div class="pt-6">
        <div class="my-8 lg:w-1/2 w-[80%]">
          <p class="lg:text-[35px] text-[#84240C] text-wrap font-medium text-2xl">Explore our selection of completed
            projects</p>
        </div>
        <div class="border-b mb-12 border-[#AFAFAF]"></div>

        <div class="grid lg:grid-cols-2 gap-4">
          <div>
            <img src="/images/projects/bathroom-project.jpg" alt="">
            <p class="my-3 text-medium">Bathroom</p>
          </div>
          <div>
            <img src="/images/projects/kitchen-project.jpg" alt="">
            <p class="my-3 text-medium">Kitchen</p>
          </div>
          <div>
            <img src="/images/projects/sitting-room-project.jpg" alt="">
            <p class="my-3 text-medium">Sitting Room</p>
          </div>
          <div>
            <img src="/images/projects/washbasins-project.jpg" alt="">
            <p class="my-3 text-medium">Washbasin</p>
          </div>
        </div>
        <div class="border-b my-10 border-[#AFAFAF]"></div>

        <div class="text-center">
          <NuxtLink to="/projects">
            <button class="uppercase bg-[#84240C] text-white lg:w-auto w-full rounded-full px-12 py-3 text-sm">Explore
              Projects</button>
          </NuxtLink>
        </div>

      </div>

      <div class="border-b lg:mb-20 mt-10 border-[#AFAFAF]"></div>

      <div class="pt-6">
        <div class="grid lg:grid-cols-2 gap-3">
          <div class="lg:pr-20">
            <div class="border-b lg:pb-8 border-[#AFAFAF] lg:mt-0 mt-10">
              <p class="lg:text-[35px] text-[#84240C] font-medium text-2xl lg:mb-0 mb-4"> Why Finishing Warehouse
              </p>
            </div>

            <div class=" text-[16px]">
              <p class="text-[#84240C] mb-4 mt-8">We set trends</p>
              <p class="text-[#0F0F0F]">
                Our offerings are inspired by global styles and tailored for the Nigerian market.</p>
            </div>
            <div class="text-[16px]">
              <p class="text-[#84240C] mb-4 mt-8">We ensure quality</p>
              <p class="text-[#0F0F0F]">
                Partnering with trusted international and local brands, we deliver only the best
                materials and products.
              </p>
            </div>
            <div class="text-[16px]">
              <p class="text-[#84240C] mb-4 mt-8">We focus on you</p>
              <p class="text-[#0F0F0F]">
                Personalized consultations and bespoke solutions ensure that every client’s needs are
                met.
              </p>
            </div>
            <div class="text-[16px]">
              <p class="text-[#84240C] mb-4 mt-8">We transform spaces</p>
              <p class="text-[#0F0F0F]">
                Beyond products, we deliver a lifestyle upgrade that makes every home stand out.

              </p>
            </div>
          </div>
          <div class="lg:mt-auto mt-10">
            <img class="lg:mb-4 " src="/images/Why-Finishing-Warehouse.jpg" alt="">
          </div>
        </div>
      </div>

      <div class="pt-6">
        <div class="my-8">
          <div class="border-b lg:py-8 text-center my-8 vorder-[#7D7D7D]">
            <p class="lg:text-[35px] text-[#84240C] font-medium text-2xl lg:mb-0 mb-4">Brand Partners</p>
          </div>
          <div class="hidden lg:grid grid-cols-7 gap-4">
            <div v-for="index in 7" :key="index" class="p-2">
              <img class="" :src="'/images/brands/00' + index + '.png'" alt="">
            </div>

          </div>
          <div class="lg:hidden block">
            <Carousel snap-align="start" pause-autoplay-on-hover="true" :items-to-show="7" :transition="1500"
              :items-to-scroll="1" :wrap-around="true" :autoplay="3000" :breakpoints="{
                300: {
                  itemsToShow: 2,
                  snapAlign: 'center',
                },
                400: {
                  itemsToShow: 2,
                  snapAlign: 'start',
                },
                500: {
                  itemsToShow: 7,
                  snapAlign: 'start',
                },
              }">
              <slide v-for="index in 7" :key="index">
                <div class="p-2">
                  <img class="" :src="'/images/brands/00' + index + '.png'" alt="">
                </div>
              </slide>
            </Carousel>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
