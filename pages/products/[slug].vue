<script setup>
const products = ref([
  {
    title: "WCs",
    products: [
      "Two Piece Toilet",
      "One Piece Toilet",
      "Washdown Rimless One Piece Toilet",
      "Rimless Wall Hung Toilet",
      "Vortex Wall Hung Toilet",
      "Rimless Wall Hung Toilet",
      "Rimless Wall Hung Toilet",
      "Rimless Wall Hung Toilet",
      "Wall Hung Bidets",
      "One Piece Toilet",
      "Intelligent Toilet",
      "Intelligent Toilet",
      "Wall Hung Bidets",
      "Concealed Cistern without Control Panel",
      "Round Matt Black Control Panel",
      "Long Strip Electroplated Silver Plating Control Panel",
      "Spray Silver Control Panel",
      "Round white Control Panel",
      "Wall-hung Auto-induction Urinal Real Spud",
      "Wall-hung Toilet P-trap",

    ],
    slug: "wcs"
  }, {
    title: "Washbasins",
    products: [
      "Glossy White In-counter Washbasin",
      "Oval Countertop Washbasin",
      "Counter-top Washbasin",
      "Glossy White Countertop Basin",
      "Glossy White Wall-hung Washbasin",
      "Glossy White In-counter Washbasin",
      "Glossy White In-counter Washbasin",
      "Glossy White Countertop Basin",
      "Glossy White Countertop Basin",
      "White Porcelain Art Basin",
      "White Porcelain Art Basin",
      "Counter-top Basin",
      "Double Kitchen Sink with Taphole",
      "Single Wall-hung Washbasin with Taphole",
      "Double Wall-hung Washbasin with Taphole",
      "Single Wall-hung Washbasin with Taphole",
      "Double Wall-hung Washbasin with Taphole",
      "Counter-top Washbasin",
      "Counter-top Washbasin with Storage Space",
      "Counter-top Washbasin",
    ],
    slug: "washbasins"
  }, {
    title: "Taps & Mixers",
    products: [
      "Basin Mixer",
      "Basin Mixer",
      "Concealed  Basin Mixer",
      "Concealed  Basin Faucet",
      "Basin Mixer",
      "Wall Hung Bathtub Mixer",
      "Concealed Basin Faucet in Chrome Design",
      "Medium Basin Mixer in Matt Black",
      "Medium Basin Mixer in Chrome",
      "Medium Basin Mixer in Grey",
      "Kitchen Faucet for Mixed and Filtered Water",
      "Floor Bathtub Mixer in Chrome ",
      "Floor Bathtub Mixer in Nickel Brush",
      "Bathroom Wall-hung Faucet with Temperature Display",
      "High Basin Mixer in Gun Grey"
    ],
    slug: "taps-mixers"
  }, {
    title: "Showers",
    products: [
      "3-way Concealed Shower in Matt Black",
      "2-way Concealed Shower in Matt Black",
      "Surface Shower in Chrome",
      "2-way Concealed Shower in Chrome",
      "2-way  Concealed Shower in Gun Grey",
      "Surface Shower in chrome Stainless Steel",
      "Surface Shower in Matt Black",
      "Surface Shower in Matt Black",
      "Surface Shower in Matt Black",
      "Surface Shower in Matt Black",
      "2-way Concealed Shower in Nickel Brush",
      "3-way Concealed Shower in Chrome",
      "2-way Concealed Shower in Chrome",
      "3-way Concealed Shower in Gun Grey Stainless Steel"
    ],
    slug: "showers"
  }, {
    title: "Accessories",
    products: [
      "Square Floor Drain ",
      "Towel Ring Chrome",
      "Toilet Paper Holder",
      "Towel Shelf ",
      "Single Towel Hanger ",
      "Rectangular Shower Drain",
      "Towel Ring in Matt Black",
      "Magnifying Glass",
      "Pop-up Drain",
      "Hand Shower",
      "Wall Mounted Hair Dryer",
      "Shower Tube",
      "Soap Dispenser in Matte",
      "Tumbler Holder and Tumbler",
      "Toilet Brush ",
      "Grab bar",
      "Robe Hook in Matt Black",
      "Place Holder in Matt Black",
      "Floor drainer (stainless steel)",
      "Floor drainer (stainless steel)",
      "Oval-shaped LED Mirror",
      "Rectangular LED Mirror",
      "Square LED Mirror",
    ],
    slug: "accessories"
  }
])

const route = useRoute()
const activeCategory = computed(() => products.value.find(p => p.slug === route.params.slug) || null)
</script>

<template>

  <div v-if="activeCategory">
    <Head>
      <title>{{ activeCategory.title }} - Finishing Warehouse</title>
    </Head>
    <!-- <HeroComp :img="1" :text="activeCategory.title" /> -->
    <div class="lg:px-20 lg:py-20 py-12 px-4 my-20">
      <p class="lg:text-4xl text-[#84240C] mb-6 font-semibold text-3xl">{{ activeCategory.title }}</p>
      <div class="border-b my-6 border-[#DEDEDE]"></div>

      <div class="grid lg:grid-cols-4 grid-cols-2 gap-4">
        <div v-for="(product, idx) in activeCategory.products" :key="idx">
          <div class="border border-[#DEDEDE] lg:h-[300px] h-[200px] flex items-center justify-center">
            <img class="lg:h-[230px] my-auto h-[200px] w-[80%] mx-auto object-scale-down"
              :src="'/images/products/' + activeCategory.slug + '/img-' + (idx + 1) + '.jpg'" alt="">
          </div>
          <p class="p-2 lg:text-[16px] text-[#0F0F0F] mt-2">{{ product }}</p>

        </div>
      </div>
    </div>
  </div>
</template>