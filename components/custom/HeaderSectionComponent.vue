<script setup>
import ButtonComponent from '@/components/custom/ButtonComponent.vue';
import PlayButtonComponent from '@/components/custom/PlayButtonComponent.vue';
import arrow from "@/assets/icons/arrow-right.svg";

const text = [
    { name: 'Answer Inquiries' },
    { name: 'Manage Calls' },
    { name: 'Schedule Reminders' },
    { name: 'Automate Invoicing' },
    { name: 'Retrieve Payment info' },
]
</script>

<template>
    <div>
        <!-- texts them them -->
        <div class="w-[1204px]">
            <h1 class="text-green mb-[32px] text-heading1 text-center">Your All-in-One Invoicing Tool</h1>
            <p class="w-[840px] mx-auto mb-[88px] text-green text-body-lg text-center">The ultimate platform tailored for small businesses, offering seamless invoice management, swift payments, and financial automation in one place.</p>
        </div>
        <!-- CTA -->
        <div class="flex items-center w-[314px] mx-auto mb-[88px]"> 
            <button-component
          text="Get Started"
          :icon="arrow"
          class="bg-green text-lemon hover:bg-[#0e2e28db] mr-[24px]"
        />
            <play-button-component />
        </div>
        
        <div class="flex items-center justify-center">
            <div v-for="(lists, index) in text" :key="index" class="mr-[36px]">
                <p class="text-black text-body-sm">{{ lists.name }}</p>
            </div>
        </div>
    </div>
</template>