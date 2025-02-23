<script setup>
import NavbarComponent from "@/components/custom/NavbarComponent.vue";
import FooterComponent from "@/components/custom/FooterComponent.vue";
</script>

<template>
  <div class="bg-background">
    <div class="w-[1440px] px-[118px] mb-[112px] mx-auto">
      <navbar-component />
      <nuxt-page />
      <footer-component />
    </div>
  </div>
</template>
