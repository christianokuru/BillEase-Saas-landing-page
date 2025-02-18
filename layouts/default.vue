<script setup>
import NavbarComponent from "@/components/custom/NavbarComponent.vue";
import FooterComponent from "@/components/custom/FooterComponent.vue";
</script>

<template>
  <main class="border w-[1440px] mx-auto">
    <navbar-component />
    <nuxt-page />
    <footer-component />
  </main>
</template>
