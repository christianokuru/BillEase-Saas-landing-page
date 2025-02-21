<script setup>
import { ref, computed, onMounted, onBeforeUnmount } from "vue";
import first from "@/assets/images/1.svg";
import second from "@/assets/images/2.svg";
import third from "@/assets/images/3.svg";
import fourth from "@/assets/images/4.svg";
import fifth from "@/assets/images/5.svg";
import sixth from "@/assets/images/6.svg";

const images = [first, second, third, fourth, fifth, sixth];
const screenWidth = ref(1440); // Default width (for SSR safety)

// Function to update screen width (only in the browser)
const updateScreenWidth = () => {
  if (typeof window !== "undefined") {
    screenWidth.value = window.innerWidth;
  }
};

onMounted(() => {
  updateScreenWidth(); // Set initial value on mount
  window.addEventListener("resize", updateScreenWidth);
});

onBeforeUnmount(() => {
  window.removeEventListener("resize", updateScreenWidth);
});

// Compute displayed images based on screen size
const displayedImages = computed(() => {
  return screenWidth.value <= 640 ? images.slice(0, 3) : images;
});
</script>

<template>
  <div class="bg-green w-[1440px] flex items-center space-x-[79.6px] px-[221px] py-[47.57px] mb-[160px] max-sm:mb-[64px] max-sm:w-[375px] max-sm:px-1 max-sm:ml-[-24px]">
    <div v-for="(image, index) in displayedImages" :key="index" class="max-sm:mx-[12px]">
      <img :src="image" alt="sponsor-logo" class="space-x-[79.6px]">
    </div>
  </div>
</template>
