<script setup>
import { ref } from 'vue';

const items = [
  {
    title: "Consultation",
    text: "We begin by understanding your needs, preferences, and project goals. This discovery phase ensures we’re aligned with your vision"
  },
  {
    title: "Design Inspiration",
    text: "Our team provides tailored recommendations and design concepts, drawing inspiration from global trends and your unique style."
  },
  {
    title: "Product Selection",
    text: "Browse our extensive range of premium materials, carefully curated to fit diverse tastes and budgets."
  },
  {
    title: "Delivery & Support",
    text: "With efficient logistics and post-purchase support, we ensure your materials are delivered on time and installed to perfection."
  },
]

const activeIndex = ref(null);

const toggle = (index) => {
  activeIndex.value = activeIndex.value === index ? null : index;
};
</script>

<template>
  <div class="accordion">
    <div v-for="(item, index) in items" :key="index" class="border-b border-[#7D7D7D]">
      <button @click="toggle(index)"
        class="accordion-header w-full text-left py-4 flex justify-between items-center">
        <span class="font-semibold text-[#0F0F0F] lg:text-xl text-lg">{{ item.title }}</span>
        <span class="text-xl">
          <img v-if="activeIndex === index" src="/images/minus.png" class="w-6" alt="">
          <img v-else src="/images/plus.png" class="w-6" alt="">
        </span>
      </button>
      <div v-show="activeIndex === index"
        class="accordion-body py-4 text-gray-700 transition-opacity duration-300">
        {{ item.text }}
      </div>
    </div>
  </div>
</template>

<style scoped>
.accordion-body {
  overflow: hidden;
  transition: max-height 0.3s ease, opacity 0.3s ease;
}
</style>
