<script>
import { defineComponent, reactive } from "vue";

export default defineComponent({
  setup() {
    const data = reactive([
      {
        title: "Kitchens",
        text: `<p>
          <strong>Countertops</strong> <br />
          Luxurious granite, marble, and quartz surfaces that combine durability with timeless elegance.
          <br /><br />
          <strong>Cabinetry</strong> <br />
          Sleek, functional, and customizable storage solutions for every kitchen layout.
          <br /><br />
          <strong>Fittings & Accessories</strong> <br />
          From pull-out pantry systems to soft-close hinges, we enhance the utility of every kitchen.
        </p>`
      },
      {
        title: "Bathrooms",
        text: `<p>
          <strong>Sanitary Ware</strong> <br />
          High-quality basins, toilets, and bidets that prioritize comfort and design.
          <br /><br />
          <strong>Tiles</strong> <br />
          A curated selection of floor and wall tiles that redefine elegance and practicality.
          <br /><br />
          <strong>Fixtures & Fittings</strong> <br />
          Statement bathtubs, rainfall showers, and designer faucets that elevate your bathroom experience.
        </p>`
      },
      {
        title: "Design Consultancy",
        text: `<p>Our expert consultants work closely with clients to bring their kitchen and bathroom dreams to life. From concept to completion, we ensure every detail aligns with your vision.</p>`
      },
      {
        title: "Design Showroom Experience",
        text: `<p>Immerse yourself in our state-of-the-art showroom, where inspiration meets reality. Explore fully styled kitchen and bathroom setups that showcase our products’ potential.</p>`
      }
    ])

    return {
      data
    }
  }
})
</script>


<template>

  <Head>
    <Title>What We Do - Finishing Warehouse </Title>
  </Head>
  <main>
    <HeroComp img="wwo" text="What We offer" />

    <section class="lg:px-20 px-4 pt-20 pb-10">
      <div v-for="(item, index) in data" :key="index" class="lg:flex mb-12">
        <img :src="`/images/wwd/00${index + 1}.png`" class="lg:w-1/2" alt="">
        <div class="bg-[#F0F0F0] lg:p-10 p-6 lg:w-1/2">
          <p class="text-[#84240C] mb-10 lg:text-[30px] text-2xl">
            {{ item.title }}
          </p>
          <div v-html="item.text" class="text-[#0F0F0F]"></div>
        </div>
      </div>
    </section>
  </main>
</template>