<template>

  <Head>
    <Title>Projects - Finishing Warehouse </Title>
  </Head>
  <div>
    <HeroComp img="projects" text="Projects" />
    <section>
      <div class="lg:px-20 px-4 lg:py-20 py-12">
        <p class="lg:text-[35px] text-[#84240C] font-medium text-2xl lg:mb-0 mb-4"> Bathroom</p>
        <div class="grid lg:grid-cols-3 gap-4 mt-8">
          <div v-for="value in 3" :key="value">
            <img :src="`/images/projects/bathroom-${value}.jpg`" alt="" />
          </div>
        </div>
      </div>
      <div class="border-b border-[#AFAFAF]"></div>

      <div class="lg:px-20 px-4 lg:py-20 py-12">
        <p class="lg:text-[35px] text-[#84240C] font-medium text-2xl lg:mb-0 mb-4"> Kitchen</p>
        <div class="grid lg:grid-cols-3 gap-4 mt-8">
          <div v-for="value in 3" :key="value">
            <img :src="`/images/projects/kitchen-${value}.jpg`" alt="" />
          </div>
        </div>
      </div>
      <div class="border-b border-[#AFAFAF]"></div>

      <div class="lg:px-20 px-4 lg:py-20 py-12">
        <p class="lg:text-[35px] text-[#84240C] font-medium text-2xl lg:mb-0 mb-4"> Sitting Room</p>
        <div class="grid lg:grid-cols-3 gap-4 mt-8">
          <div v-for="value in 3" :key="value">
            <img :src="`/images/projects/sitting-room-${value}.jpg`" alt="" />
          </div>
        </div>
      </div>
      <div class="border-b border-[#AFAFAF]"></div>

      <div class="lg:px-20 px-4 lg:py-20 py-12">
        <p class="lg:text-[35px] text-[#84240C] font-medium text-2xl lg:mb-0 mb-4">Washbasin</p>
        <div class="grid lg:grid-cols-3 gap-4 mt-8">
          <div v-for="value in 3" :key="value">
            <img :src="`/images/projects/washbasin-${value}.jpg`" alt="" />
          </div>
        </div>
      </div>
      <div class="border-b border-[#AFAFAF]"></div>
    </section>
  </div>
</template>