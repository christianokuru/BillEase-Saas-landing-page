<script setup>
import NavbarComponent from "@/components/custom/NavbarComponent.vue";
import FooterComponent from "@/components/custom/FooterComponent.vue";
</script>

<template>
  <div class="bg-background">
    <main class="max-sm:w-[375px] max-sm:px-[24px] w-[1440px] px-[118px] mx-auto">
    <navbar-component />
    <nuxt-page />
    <footer-component />
  </main>
  </div>
</template>
