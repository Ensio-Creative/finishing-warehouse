<script setup>
const slider = ref([
  {
    title: "Bathroom Finish",
    des: "Transform your bathroom into a luxurious oasis with our range of high-quality bathroom solutions. From sleek faucets and modern vanities to elegant showers and stylish accessories, we have everything you need to create the perfect retreat."
  },
  {
    title: "Wall Finish",
    des: "Make a statement with our collection of wall finishing materials. Enhance your walls with our eco-friendly materials made from sustainable and recycled materials. From tiles to reclaimed wood panels, we offer a variety of options to help you create luxurious spaces."
  },
  {
    title: "Kitchen Finish",
    des: "Elevate your kitchen with our premium kitchen fittings and accessories. Whether you're looking for durable sinks, stylish faucets, or innovative storage solutions, we have a wide selection of products to suit every taste and budget."
  },
  {
    title: "Outdoor Finish",
    des: "Transform your outdoor spaces with our durable and weather-resistant finishing materials. From decking to fencing, we offer a wide range of options to help you create the perfect outdoor oasis for relaxing and entertaining."
  },
  {
    title: "Home Decor",
    des: "Add personality and style to your home with our curated selection of decorative elements. From rugs to wall art, we have everything you need to make your space uniquely yours."
  },
  {
    title: "Lighting ",
    des: "Illuminate your space with our exquisite but energy-efficient lighting fixtures that help reduce energy consumption and lower your carbon footprint. From chic chandeliers and pendants to energy efficient LED smart lighting systems, we offer eco-friendly lighting solutions to enhance your home."
  },
  {
    title: "Curtains",
    des: "Add the perfect finishing touch to your windows with our exquisite collections of curtains and blinds. Choose from variety of fabrics, colors, and styles to complement your decor and create the perfect atmosphere in any room."
  }
])
</script>

<template>

  <Head>
    <Title>Products - Finishing Warehouse </Title>
  </Head>
  <div>
    <HeroComp img="products" text="Product Categories" />
    <div class="lg:px-20 px-4 py-10">
      <!-- <p class="lg:text-4xl text-3xl font-semibold">Product Categories</p> -->
      <!-- <p>Explore our product categories.</p> -->


      <div v-for="slide in 7" :key="slide" class="my-6 relative">
        <NuxtLink :to="'/products/' + slide">
          <img class=" lg:h-auto " :src="'/images/products/product' + slide + '.png'" alt="">
          <div class="lg:absolute bottom-0 lg:p-10 p-6 left-0 bg-[#0F0F0F] lg:w-[50%]">
            <p class=" lg:text-3xl text-2xl my-1 text-white">{{ slider[slide - 1].title }}</p>
            <p class="text-white text-sm">{{ slider[slide - 1].des }}</p>
          </div>
        </NuxtLink>
      </div>
      <!-- <div class="my-6 relative">
        <img class=" lg:h-auto h-72" src="/images/products/product2.png" alt="">
        <p class="absolute bottom-6 lg:left-10 left-4 lg:text-4xl text-2xl text-white">Wall Finish</p>
      </div>
      <div class="my-6 relative">
        <img class=" lg:h-auto h-72" src="/images/products/product3.png" alt="">
        <p class="absolute bottom-6 lg:left-10 left-4 lg:text-4xl text-2xl text-white">Kitchen Finish</p>
      </div>
      <div class="my-6 relative">
        <img class=" lg:h-auto h-72" src="/images/products/product4.png" alt="">
        <p class="absolute bottom-6 lg:left-10 left-4 lg:text-4xl text-2xl text-white">Indoor Finish</p>
      </div>
      <div class="my-6 relative">
        <img class=" lg:h-auto h-72" src="/images/products/product5.png" alt="">
        <p class="absolute bottom-6 lg:left-10 left-4 lg:text-4xl text-2xl text-white">Outdoor Finish</p>
      </div>
      <div class="my-6 relative">
        <img class=" lg:h-auto h-72" src="/images/products/product6.png" alt="">
        <p class="absolute bottom-6 lg:left-10 left-4 lg:text-4xl text-2xl text-white">Home Decor</p>
      </div>
      <div class="my-6 relative">
        <img class=" lg:h-auto h-72" src="/images/products/product7.png" alt="">
        <p class="absolute bottom-6 lg:left-10 left-4 lg:text-4xl text-2xl text-white">Lighting</p>
      </div>
      <div class="my-6 relative">
        <img class=" lg:h-auto h-72" src="/images/products/product8.png" alt="">
        <p class="absolute bottom-6 lg:left-10 left-4 lg:text-4xl text-2xl text-white">Curtains</p>
      </div> -->
    </div>
  </div>
</template>