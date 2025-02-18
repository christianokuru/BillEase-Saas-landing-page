<script setup>
import LogoComponent from "@/components/custom/LogoComponent.vue";
import ButtonComponent from "@/components/custom/ButtonComponent.vue";
import arrow from "@/assets/icons/arrow-right.svg";
import { navlinks } from "@/lib/navlinks.js";
</script>

<template>
  <div class="mb-[122px]">
    <div class="flex items-center mt-[40px] mb-[10px]">
      <div class="mr-[266px]">
        <logo-component />
      </div>

      <div class="flex items-center mr-[250px]">
        <nav v-for="links in navlinks" :key="links.text">
          <nuxt-link
            :to="links.route"
            class="mr-[36px] text-green text-[16px] hover:border-b-2"
            >{{ links.text }}</nuxt-link
          >
        </nav>
      </div>

      <div class="">
        <button-component
          text="Sign In"
          :icon="arrow"
          class="bg-green text-lemon hover:bg-[#0e2e28db]"
        />
      </div>
    </div>
  </div>
</template>
