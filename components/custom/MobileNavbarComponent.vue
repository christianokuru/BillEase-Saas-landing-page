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
      class="bg-white shadow-lg rounded-lg p-4 absolute  left-0 top-16"
    >
      <nav v-for="links in navlinks" :key="links.text">
        <nuxt-link
          :to="links.route"
          class="block py-2 text-green text-[16px] hover:border-b-2"
          >{{ links.text }}</nuxt-link
        >
      </nav>

      <!-- Sign In Button (Mobile) -->
      <div class="mt-4">
        <button-component
          text="Sign In"
          :icon="arrow"
          class="bg-green text-lemon hover:bg-[#0e2e28db]"
        />
      </div>
    </div>
  </div>
</template>
