<!-- components/custom/MobileNavbar.vue -->
<script setup>
import { ref } from "vue";
import { navlinks } from "@/lib/navlinks.js";
import ButtonComponent from "@/components/custom/ButtonComponent.vue";
import arrow from "@/assets/icons/arrow-right.svg";
import hamburger from "@/assets/icons/hamburger.svg";

// State for menu toggle
const isMenuOpen = ref(false);

// Toggle function
const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
};
</script>

<template>
  <div class="sm:hidden">
    <!-- Mobile Menu Button -->
    <button @click="toggleMenu">
      <img v-if="!isMenuOpen" :src="hamburger" alt="" />
      <svg
        v-else
        class="w-6 h-8 text-red-600"
        fill="none"
        stroke="currentColor"
        viewBox="0 0 24 24"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          d="M6 18L18 6M6 6l12 12"
        />
      </svg>
    </button>

    <!-- Mobile Navigation Dropdown -->
    <div
      v-if="isMenuOpen"
      class="w-full bg-white shadow-lg p-4 pt-[40px] absolute left-0 top-0"
    >
      <div class="mb-[43px]">
        <button @click="toggleMenu" class="pl-[22rem]">
          <img v-if="!isMenuOpen" src="" alt="" />
          <svg
            v-else
            class="w-6 h-8 text-red-600"
            fill="none"
            stroke="currentColor"
            viewBox="0 0 24 24"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M6 18L18 6M6 6l12 12"
            />
          </svg>
        </button>
      </div>
      <nav v-for="links in navlinks" :key="links.text" class="mb-[19px]">
        <nuxt-link
          :to="links.route"
          class="block py-2 text-green text-body-md hover:underline"
          >{{ links.text }}</nuxt-link
        >
      </nav>

      <!-- Sign In Button (Mobile) -->
      <div class="mt-[62px]">
        <button-component
          text="Sign In"
          :icon="arrow"
          class="bg-green text-lemon hover:bg-[#0e2e28db]"
        />
      </div>
    </div>
  </div>
</template>
