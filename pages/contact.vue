<template>
  <Head>
    <Title>Contact - Finishing Warehouse </Title>
  </Head>
  <div>
    <HeroComp img="contact" />
    <div class="lg:px-24 px-4 py-12">
      <p class="lg:text-4xl text-2xl font-semibold">Get in touch</p>
      <p class="lg:w-[40%] mt-3">For enquiry, quotation, or feedback, get in touch with us and we will be glad to hear from
        and respond as soon as
        we can.</p>
      <div class="lg:flex justify-between my-10">
        <div class="border lg:my-0 my-3 lg:w-[32%] border-[#CBCBCB] p-6 h-52">
          <img src="/images/icons/img-1.png" class="w-10" alt="">
          <p class="mt-14 text-xl">Suite D28, Efab Mall, Garki, <br>
            Area 11, FCT, Abuja</p>
        </div>
        <div class="border lg:my-0 my-3 lg:w-[32%] border-[#CBCBCB] p-6">
          <img src="/images/icons/img-2.png" class="w-10" alt="">
          <p class="mt-20 text-xl">info@finishingwarehouse.com</p>
        </div>
        <div class="border lg:my-0 my-3 lg:w-[32%] border-[#CBCBCB] p-6">
          <img src="/images/icons/img-3.png" class="w-10" alt="">
          <p class="mt-20 text-xl">+234 9052766460</p>
        </div>
      </div>
      <div class="bg-[#000000] lg:mb-10 px-8 lg:py-16 py-10">
        <div class="lg:flex lg:my-6 justify-between">
          <div class="lg:w-[48%]">
            <input type="text" placeholder="First Name*"
              class="w-full bg-transparent border-b border-[#FFFFFF] p-4 focus:outline-none text-white text-sm">
          </div>
          <div class="lg:w-[48%]">
            <input type="text" placeholder="Last Name*"
              class="w-full bg-transparent border-b border-[#FFFFFF] p-4 focus:outline-none text-white text-sm">
          </div>
        </div>
        <div class="lg:flex lg:my-6 justify-between">
          <div class="lg:w-[48%]">
            <input type="text" placeholder="Email Address"
              class="w-full bg-transparent border-b border-[#FFFFFF] p-4 focus:outline-none text-white text-sm">
          </div>
          <div class="lg:w-[48%]">
            <input type="text" placeholder="Phone Number*"
              class="w-full bg-transparent border-b border-[#FFFFFF] p-4 focus:outline-none text-white text-sm">
          </div>
        </div>
        <div class="my-8">
          <textarea placeholder="Your Message*"
            class="p-4 text-sm border text-white border-white h-72 focus:outline-none w-full bg-transparent"></textarea>
        </div>
        <button class="bg-[#FBC06B] w-full p-3">SEND MESSAGE</button>
      </div>
    </div>
  </div>
</template>