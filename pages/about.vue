<template>

  <Head>
    <Title>About - Finishing Warehouse </Title>
  </Head>
  <div class="">
    <HeroComp img="about" text="About us" />
    <div class="lg:flex lg:px-20 px-4 lg:py-20 py-12">
      <div class="lg:w-[50%] lg:mr-10">
        <p class="lg:text-[35px] text-[#84240C] text-2xl font-medium mb-4">Finishing that Speak</p>
        <p class="">
          At Finishing Warehouse Nigeria Limited, we specialize in crafting bathrooms and kitchens that inspire and
          elevate lifestyles. Based in the vibrant city of Abuja, Nigeria, our mission is simple yet profound: to
          redefine spaces by delivering finishing materials that transform the ordinary into the extraordinary.
           <br> <br>
          Your kitchen is more than a cooking space; it’s the heart of your home, where memories are made. Your bathroom
          is more than a utility; it’s a sanctuary for relaxation and renewal. We understand this, and every product we
          offer is meticulously selected to bring these visions to life.
        </p>
      </div>
      <div class="lg:w-[50%] lg:mt-0 mt-6">
        <img src="/images/About-Bathroom.jpg" class="w-full h-full object-cover" alt="">
      </div>
    </div>

    <section class="grid lg:grid-cols-3 gap-3 lg:px-20 px-4 pb-12">
      <div class="bg-[#F0F0F0] px-6 py-12">
        <p class="lg:text-[35px] text-2xl text-[#84240C] mb-10">Our Vision</p>
        <p class="text-[#0F0F0F] text-lg">To be Nigeria’s premier destination for innovative kitchen and bathroom
          solutions that blend style, functionality, and sustainability.</p>
      </div>
      <img src="/images/vision-mission.png" alt="">
      <div class="bg-[#F0F0F0] px-6 py-12">
        <p class="lg:text-[35px] text-2xl text-[#84240C] mb-10">Our Mission</p>
        <p class="text-[#0F0F0F] text-lg">To empower homeowners, designers, and developers to create bespoke kitchen and
          bathroom spaces through premium materials and unparalleled expertise.</p>
      </div>
    </section>

    <section class="lg:px-20 px-4 lg:mt-20">
      <div class="lg:w-1/2 mb-6">
        <p class="lg:text-[35px] text-[#84240C] text-2xl font-medium mb-4">Our Core Values</p>
        <p>At Finishing Warehouse, we operate on a foundation of <strong>Lifestyle Excellence</strong> through the 3i’s:
        </p>
      </div>
      <div class="border-y border-[#7D7D7D] flex justify-between py-6">
        <p class="lg:my-auto text-[20px] ">Innovation</p>
        <p class="lg:w-1/2 w-[62%]">Staying ahead of global trends to bring cutting-edge designs and technologies to our
          clients.
        </p>
      </div>
      <div class="border-b border-[#7D7D7D] flex justify-between py-6">
        <p class="lg:my-auto text-[20px] ">Ingenuity</p>
        <p class="lg:w-1/2 w-[62%]">Offering customized solutions that cater to the unique needs and
          tastes of every project.</p>
      </div>
      <div class="border-b border-[#7D7D7D] flex justify-between py-6">
        <p class="lg:my-auto text-[20px] ">Integrity</p>
        <p class="lg:w-1/2 w-[62%]">Building lasting relationships through trust, quality, and impeccable service.</p>
      </div>
    </section>
    <div class="lg:px-20 px-4 py-20">
      <img class="lg:h-auto h-[50vh] object-cover" src="/images/about-2.png" alt="">
    </div>

    <section class="lg:flex justify-between lg:px-20 px-4 pb-16">
      <div class="lg:w-[45%]">
        <p class="lg:text-[35px] text-[#84240C] text-2xl font-medium mb-4">The Finishing Warehouse Experience</p>
        <div class="border-b border-[#7D7D7D] mt-10"></div>
        <Accordion />
      </div>
      <img class="lg:w-1/2 lg:mt-0 mt-4" src="/images/experience.png" alt="">
    </section>

    <section class="lg:px-20 px-4 pb-12">
      <p class="lg:text-[35px] text-[#84240C] text-2xl font-medium mb-8">Our Milestones</p>
      <div class="grid lg:grid-cols-3 gap-4">
        <div class="lg:mb-0 mb-5">
          <img src="/images/milestone/milestones-1.png" alt="">
          <p class="text-[#0F0F0F] lg:w-[90%] lg:mt-6 mt-3">Supplied bespoke kitchen and bathroom solutions for luxury
            estates
            and
            commercial projects across Nigeria.
          </p>
        </div>
        <div class="lg:mb-0 mb-5">
          <img src="/images/milestone/milestones-2.png" alt="">
          <p class="text-[#0F0F0F] lg:w-[90%] lg:mt-6 mt-3">Introduced innovative products such as eco-friendly basins
            and
            water-saving
            sanitary wares to the Nigerian market.
          </p>
        </div>
        <div>
          <img src="/images/milestone/milestones-3.png" alt="">
          <p class="text-[#0F0F0F] lg:w-[90%] lg:mt-6 mt-3">Recognized as a trusted partner by leading developers,
            architects,
            and interior
            designers.
          </p>
        </div>
      </div>
    </section>
    <div class="border-b lg:mx-20 border-[#AFAFAF]"></div>

    <section class="lg:px-20 py-20 p-4">
      <div class="lg:w-1/2 mx-auto mb-20 text-center">
        <p class="lg:text-[35px] text-[#84240C] mb-4 text-2xl font-medium">Our Team Members</p>
        <p class="text-[#0F0F0F]">Meet our dedicated team at Finishing Warehouse, where passion, professionalism, and a
          commitment to sustainability drive us to deliver eco-friendly, high-quality solutions that bring your vision
          to life.</p>
      </div>
      <div class="grid lg:grid-cols-4 gap-4">
        <div class="text-center">
          <img class="mx-auto" src="/images/team/img-1.png" alt="">
          <p class="text-[#0F0F0F] mt-4 font-medium">Engr. Nnnanna Ogbuja</p>
          <p class="text-[#0F0F0F] text-sm">MANAGING DIRECTOR</p>
        </div>
        <div class="text-center">
          <img class="mx-auto" src="/images/team/img-2.png" alt="">
          <p class="text-[#0F0F0F] mt-4 font-medium">Mrs. Julieth Obe</p>
          <p class="text-[#0F0F0F] text-sm">FINANCIAL ANALYST</p>
        </div>
        <div class="text-center">
          <img class="mx-auto" src="/images/team/img-3.png" alt="">
          <p class="text-[#0F0F0F] mt-4 font-medium">Mr. Raji Elijah</p>
          <p class="text-[#0F0F0F] text-sm">WAREHOUSE OFFICER</p>
        </div>
        <div class="text-center">
          <img class="mx-auto" src="/images/team/img-4.png" alt="">
          <p class="text-[#0F0F0F] mt-4 font-medium">Ms. Rita Okoye</p>
          <p class="text-[#0F0F0F] text-sm">HEAD OF SALE & MARKETING</p>
        </div>
      </div>
    </section>
    <!-- <div class="lg:flex lg:w-[78%] mb-12 mx-auto justify-between">
      <img class="lg:mb-0 mb-3" src="/images/abt-1.png" alt="">
      <img src="/images/abt-2.png" alt="">
    </div> -->
  </div>
</template>