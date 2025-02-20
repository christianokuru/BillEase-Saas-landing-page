<script setup>
import ButtonComponent2 from "@/components/custom/ButtonComponent2.vue";
</script>

<template>
  <div class="mb-[160px]">
    <div class="flex items-center justify-between w-[1008px] ml-[95px]">
      <div>
        <!-- text div -->
        <div class="w-[493px]">
          <div>
            <h1
              class="text-green text-heading2 w-[475px] leading-[56px] mb-[24px]"
            >
              One seamless invoice at a time.
            </h1>
          </div>
          <div>
            <p class="text-green w-[445px] text-body-lg leading-[28px]">
              Thrive with efficient invoicing, ensuring you stay on growth, not
              paperwork.
            </p>
          </div>

          <div class="flex items-center mt-[49px] w-[439px]">
            <button-component2
              text="Unlimited Capacity"
              class="bg-lemon text-green w-[223px] font-[600] mr-[24px] hover:bg-[#d1eb089d]"
            />
            <button-component2
              text="24/7 availability"
              class="bg-lemon text-green w-[223px] font-[600] hover:bg-[#d1eb089d]"
            />
          </div>
        </div>
      </div>
      <!-- right div -->
      <div class="w-[324px]">
        <p class="border-b border-green pb-[40.45px] text-green text-body-lg">Create and send invoices in seconds</p>
        <p class="border-b border-green py-[40.45px] text-green text-body-lg">Pay bills on time without missing a beat</p>
        <p class="pt-[40.45px] text-green text-body-lg">Control your cash flow on-demand</p>
      </div>
    </div>
  </div>
</template>
