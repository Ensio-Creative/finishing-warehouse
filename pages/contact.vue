<template>
  <Head>
    <Title>Contact - Finishing Warehouse </Title>
  </Head>
  <div>
    <HeroComp img="contact" />
    <div class="lg:px-24 px-4 py-12">
      <p class="text-4xl">Get in touch</p>
      <p class="lg:w-80 mt-3">For enquiry, quotation, or feedback, get in touch with us and we will be glad to hear from
        and respond as soon as
        we can.</p>
      <div class="lg:flex justify-between my-10">
        <div class="border lg:my-0 my-3 lg:w-[32%] border-[#7D7D7D] p-6">
          <img src="/images/icons/img-1.png" class="w-10" alt="">
          <p class="mt-2">Suite D28, Efab Mall, Garki, <br>
            Area 11, FCT, Abuja</p>
        </div>
        <div class="border  lg:my-0 my-3 lg:w-[32%] border-[#7D7D7D] p-6">
          <img src="/images/icons/img-2.png" class="w-10" alt="">
          <p class="mt-6">info@finishingwarehouse.com</p>
        </div>
        <div class="border  lg:my-0 my-3 lg:w-[32%] border-[#7D7D7D] p-6">
          <img src="/images/icons/img-3.png" class="w-10" alt="">
          <p class="mt-6">+234 9052766460</p>
        </div>
      </div>
      <div class="bg-[#000000] mb-10 p-8">
        <div class="flex my-6 justify-between">
          <div class="w-[48%]">
            <input type="text" placeholder="First Name*"
              class="w-full bg-transparent border-b border-[#FFFFFF] p-4 focus:outline-none text-white text-sm">
          </div>
          <div class="w-[48%]">
            <input type="text" placeholder="Last Name*"
              class="w-full bg-transparent border-b border-[#FFFFFF] p-4 focus:outline-none text-white text-sm">
          </div>
        </div>
        <div class="flex my-6 justify-between">
          <div class="w-[48%]">
            <input type="text" placeholder="Email Address"
              class="w-full bg-transparent border-b border-[#FFFFFF] p-4 focus:outline-none text-white text-sm">
          </div>
          <div class="w-[48%]">
            <input type="text" placeholder="Phone Number*"
              class="w-full bg-transparent border-b border-[#FFFFFF] p-4 focus:outline-none text-white text-sm">
          </div>
        </div>
        <div class="my-8">
          <textarea placeholder="Your Message*"
            class="p-4 text-sm border border-white h-44 focus:outline-none w-full bg-transparent"></textarea>
        </div>
        <button class="bg-[#FBC06B] w-full p-3">SEND MESSAGE</button>
      </div>
    </div>
  </div>
</template>