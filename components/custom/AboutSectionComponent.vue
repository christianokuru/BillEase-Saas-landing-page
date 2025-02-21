<script setup>
import ButtonComponent2 from "@/components/custom/ButtonComponent2.vue";
</script>

<template>
  <div class="mb-[160px] max-sm:w-[349px] max-sm:my-[64px]  max-sm:px-[0px]">
    <div
      class="flex items-center justify-between w-[1008px] ml-[95px] max-sm:w-[327px] max-sm:ml-[0px] max-sm:flex-col"
    >
      <div class="max-sm:w-[327px] max-sm:mb-[88px]">
        <!-- text div -->
        <div class="w-[493px]max-sm:w-[327px]">
          <div class="max-sm:w-[327px] max-sm:mb-[24px]">
            <h1
              class="text-green text-heading2 w-[475px] leading-[56px] mb-[24px] max-sm:text-sub-heading max-sm:w-[327px] max-sm:text-left max-sm:leading-[48px]"
            >
              One seamless invoice at a time.
            </h1>
          </div>
          <div>
            <p
              class="text-green w-[445px] text-body-lg leading-[28px] max-sm:w-[327px] max-sm:text-body-md"
            >
              Thrive with efficient invoicing, ensuring you stay on growth, not
              paperwork.
            </p>
          </div>

          <div
            class="flex items-center mt-[49px] w-[439px] max-sm:flex-col max-sm:w-[327px] max-sm:items-start"
          >
            <button-component2
              text="Unlimited Capacity"
              class="bg-lemon text-green font-[600] mr-[24px] hover:bg-[#d1eb089d] max-sm:mb-[16px]"
            />
            <button-component2
              text="24/7 availability"
              class="bg-lemon text-green font-[600] hover:bg-[#d1eb089d]"
            />
          </div>
        </div>
      </div>
      <!-- right div -->
      <div class="w-[324px]">
        <p class="border-b border-green pb-[40.45px] text-green text-body-lg">
          Create and send invoices in seconds
        </p>
        <p class="border-b border-green py-[40.45px] text-green text-body-lg">
          Pay bills on time without missing a beat
        </p>
        <p class="pt-[40.45px] text-green text-body-lg">
          Control your cash flow on-demand
        </p>
      </div>
    </div>
  </div>
</template>
