<script setup>
import NavbarComponent from "@/components/custom/NavbarComponent.vue";
import FooterComponent from "@/components/custom/FooterComponent.vue";
// import { ref } from 'vue';
</script>

<template>
<div class="w-[1440px] px-[118px] mb-[112px] mx-auto h-screen">
    <navbar-component />
    <nuxt-page />
    <footer-component />
</div>
</template>