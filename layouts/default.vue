<script setup>
import NavbarComponent from "@/components/custom/NavbarComponent.vue";
import FooterComponent from "@/components/custom/FooterComponent.vue";
</script>

<template>
  <div class="bg-red-200">
    <main class="border max-sm:w-[380px] max-sm:px-[24px] px-[118px] w-[1440px] mx-auto">
    <navbar-component />
    <nuxt-page />
    <footer-component />
  </main>
  </div>
</template>
