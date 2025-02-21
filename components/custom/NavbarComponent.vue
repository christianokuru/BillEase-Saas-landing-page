<script setup>
import LogoComponent from "@/components/custom/LogoComponent.vue";
import ButtonComponent from "@/components/custom/ButtonComponent.vue";
import MobileNavbarComponent from "@/components/custom/MobileNavbarComponent.vue";
import arrow from "@/assets/icons/arrow-right.svg";
import { navlinks } from "@/lib/navlinks.js";
</script>

<template>
  <div class="mb-[122px] max-sm:mb-[50px]  px-[118px] max-sm:px-[24px]">
    <div class="max-sm:pt-[36px] flex items-center justify-between pt-[40px] mb-[10px]">
      <!-- Logo -->
      <logo-component />

      <!-- Desktop Navigation -->
      <div class="flex items-center max-sm:hidden">
        <nav v-for="links in navlinks" :key="links.text">
          <nuxt-link
            :to="links.route"
            class="mr-[36px] text-green text-[16px] hover:border-b-2"
            >{{ links.text }}</nuxt-link
          >
        </nav>
      </div>

      <!-- Sign In Button (Desktop) -->
      <div class="max-sm:hidden">
        <button-component
          text="Sign In"
          :icon="arrow"
          class="bg-green text-lemon hover:bg-[#0e2e28db]"
        />
      </div>

      <!-- Mobile Navigation Component -->
      <mobile-navbar-component />
    </div>
  </div>
</template>