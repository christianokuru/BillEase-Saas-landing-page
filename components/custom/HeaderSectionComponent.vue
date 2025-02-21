<script setup>
import ButtonComponent from "@/components/custom/ButtonComponent.vue";
import PlayButtonComponent from "@/components/custom/PlayButtonComponent.vue";
import arrow from "@/assets/icons/arrow-right.svg";
import hero from "@/assets/images/header-image.png";

const text = [
  { name: "Answer Inquiries" },
  { name: "Manage Calls" },
  { name: "Schedule Reminders" },
  { name: "Automate Invoicing" },
  { name: "Retrieve Payment info" },
];
</script>

<template>
  <div>
    <div>
      <!-- texts them them -->
      <div class="w-[1204px] max-sm:w-[322px] ml-[118px] max-sm:ml-0">
        <h1 class="text-green max-sm:text-[46px] max-sm:text-left max-sm:leading-none mb-[32px] text-heading1 text-center">
          Your All-in-One Invoicing Tool
        </h1>
        <p
          class="max-sm:w-[320px] max-sm:text-body-sm max-sm:text-left max-sm:mb-[56px] w-[840px] mx-auto mb-[88px] text-green text-body-lg text-center"
        >
          The ultimate platform tailored for small businesses, offering seamless
          invoice management, swift payments, and financial automation in one
          place.
        </p>
      </div>
      <!-- CTA -->
      <div class="max-sm:mb-[56px] flex items-center w-[314px] mx-auto mb-[88px] max-sm:ml-0">
        <button-component
          text="Get Started"
          :icon="arrow"
          class="bg-green text-lemon hover:bg-[#0e2e28db] mr-[24px]"
        />
        <play-button-component />
      </div>

      <div class="max-sm:grid max-sm:grid-cols-2 max-sm:grid-rows-2 flex items-center justify-center mb-[60px]">
        <div v-for="(lists, index) in text" :key="index" class="mr-[36px] max-sm:text-nowrap max-sm:mb-[10px] max-sm:border max-sm:border-[#00000041] max-sm:mx-[7px] max-sm:rounded-full max-sm:bg-lemon">
          <p class="max-sm:pl-[3px] text-black text-body-sm">{{ lists.name }}</p>
        </div>
      </div>
    </div>

    <div>
        <div>
            <img :src="hero" alt="hero-img" class="max-sm:w-[327px] mx-auto" />
        </div>
    </div>
  </div>
</template>
