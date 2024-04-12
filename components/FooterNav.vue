<template>
  <div>
    <div class="relative">
      <img class="lg:h-auto object-cover h-[60vh]" src="/images/footer-img.png" alt="">
      <div class="absolute top-0 w-full h-full bg-gradient-to-b from-[#84240C66] to-[#000000]"></div>
      <div
        class="absolute  text-center text-white top-20 lg:w-[58%] w-[80%] mx-auto left-0 right-0 lg:px-32 px-10 lg:py-24 py-10 overlay border-[#FFFFFF33]">
        <p class="lg:text-5xl text-xl font-normal">To learn more about our
          products, pricing or
          how to place an order.</p>
        <NuxtLink to="/contact">
          <p class="underline mt-6 lg:text-base text-sm">CONTACT US</p>
        </NuxtLink>
      </div>
    </div>
    <div class="bg-[#000000] lg:px-20 px-4 py-4">
      <div class="flex justify-evenly mb-10 lg:w-[40%] mx-auto">
        <button class="text-[#7D7D7D] border border-[#7D7D7D] p-2 rounded-full lg:px-8 px-4 text-sm">Facebook</button>
        <button class="text-[#7D7D7D] border border-[#7D7D7D] p-2 rounded-full lg:px-8 px-4 text-sm">Instagram</button>
        <button class="text-[#7D7D7D] border border-[#7D7D7D] p-2 rounded-full lg:px-8 px-4 text-sm">X
          (Twitter)</button>
      </div>
      <div class="lg:flex justify-between lg:text-left text-center py-8 text-white text-sm">
        <p>Copyright © 2024 - Finishing Warehouse </p>
        <p class="lg:mt-0 mt-4">Designed by <a href="https://ensiocreative.com/">Ensio Creative</a> </p>
      </div>
    </div>
  </div>
</template>

<style>
.overlay {
  background: rgba(15, 15, 15, 0.16);
  border-radius: 5px;
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
  backdrop-filter: blur(11.6px);
  -webkit-backdrop-filter: blur(11.6px);
  border: 1px solid #FFFFFF33;
}
</style>