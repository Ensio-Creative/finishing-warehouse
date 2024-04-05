<template>

  <Head>
    <Title>Contact - Finishing Warehouse </Title>
  </Head>
  <div>
    <HeroComp img="contact" />
    <div class="lg:px-24 px-4 py-12">
      <p class="lg:text-4xl text-3xl font-semibold">Get in touch</p>
      <p class="lg:w-[40%] mt-3">For enquiry, quotation, or feedback, get in touch with us and we will be glad to hear
        from
        and respond as soon as
        we can.</p>
      <!-- <div class="lg:flex justify-between my-10">
        <div class="border lg:my-0 my-3 lg:w-[32%] border-[#CBCBCB] p-6 h-52">
          <img src="/images/icons/img-1.png" class="w-10" alt="">
          <p class="mt-14 text-xl">Suite D28, Efab Mall, Garki, <br>
            Area 11, FCT, Abuja</p>
        </div>
        <div class="border lg:my-0 my-3 lg:w-[32%] border-[#CBCBCB] p-6">
          <img src="/images/icons/img-3.png" class="w-10" alt="">
          <p class="mt-20 text-xl">info@finishingwarehouse.com</p>
        </div>
        <div class="border lg:my-0 my-3 lg:w-[32%] border-[#CBCBCB] p-6">
          <img src="/images/icons/img-2.png" class="w-10" alt="">
          <p class="mt-20 text-xl">+234 9052766460</p>
        </div>
      </div> -->
      <div class="lg:flex justify-between lg:py-16 py-10 lg:mb-10 ">
        <div class="bg-[#84240C] p-6 text-white rounded-xl lg:w-[26%]">
          <div class="mb-8">
            <p class="font-bold text-lg mb-2">Office Address</p>
            <p>Suite D28, Efab Mall, Garki, Area 11, FCT, Abuja</p>
          </div>
          <div class="mb-8">
            <p class="font-bold text-lg mb-2">Abuja Showroom Address</p>
            <p>Our showroom is located on the Second Floor, Machina Plaza, Mambolo Street, Abuja</p>
          </div>
          <div class="mb-8">
            <p class="font-bold text-lg mb-2">Email</p>
            <p>info@finishingwarehouse.com</p>
          </div>
          <div>
            <p class="font-bold text-lg mb-2">Phone</p>
            <p>+234 905 276 6460</p>
          </div>
        </div>
        <div class="lg:w-[70%]">
          <div class="lg:flex lg:my-6 justify-between">
            <div class="lg:w-[48%]">
              <input type="text" placeholder="First Name*"
                class="w-full bg-transparent border-b border-[#0F0F0F] p-4 focus:outline-none text-[#0F0F0F] text-sm">
            </div>
            <div class="lg:w-[48%]">
              <input type="text" placeholder="Last Name*"
                class="w-full bg-transparent border-b border-[#0F0F0F] p-4 focus:outline-none text-[#0F0F0F] text-sm">
            </div>
          </div>
          <div class="lg:flex lg:my-6 justify-between">
            <div class="lg:w-[48%]">
              <input type="text" placeholder="Email Address"
                class="w-full bg-transparent border-b border-[#0F0F0F] p-4 focus:outline-none text-[#0F0F0F] text-sm">
            </div>
            <div class="lg:w-[48%]">
              <input type="text" placeholder="Phone Number*"
                class="w-full bg-transparent border-b border-[#0F0F0F] p-4 focus:outline-none text-[#0F0F0F] text-sm">
            </div>
          </div>
          <div class="my-8">
            <textarea placeholder="Your Message*"
              class="p-4 text-sm border text-[#0F0F0F] rounded-xl border-[#0F0F0F] h-72 focus:outline-none w-full bg-transparent"></textarea>
          </div>
          <button class="bg-[#0F0F0F] rounded-xl text-white w-full p-3">SEND MESSAGE</button>
        </div>
      </div>
    </div>
  </div>
</template>