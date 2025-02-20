<script setup>
import ButtonComponent2 from '@/components/custom/ButtonComponent2.vue';
</script>

<template>
    <div class="border">
        <div class="border border-red-500 w-[1008px] ml-[70px]">
           <div>
            <!-- text div -->
            <div class="border border-blue-500 w-[493px]">
                <div>
                    <h1 class="text-green border text-heading2 w-[475px] leading-[56px] mb-[24px]">One seamless invoice at a time.</h1>
                </div>
                <div>
                    <p class="text-green border w-[445px] text-body-lg leading-[28px]">Thrive with efficient invoicing, ensuring you stay on growth, not paperwork.</p>
                </div>
            </div>
            <!-- button div -->
            <div class="mt-[49px]">
                <button-component2 text="Unlimited Capacity"  class="bg-lemon text-green w-[223px] font-[600] mr-[24px]"/>
                <button-component2 text="24/7 availability"  class="bg-lemon text-green w-[223px] font-[600]"/>
            </div>
           </div>
           <!-- right div -->
           <div></div>
        </div>
    </div>
</template>