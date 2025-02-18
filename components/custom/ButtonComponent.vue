<script setup>
const props = defineProps({
    icon: {
        type: String,
    },
    text: {
        type: String,
        required: true
    }
})
</script>

<template>
    <button class="flex items-center text-nowrap py-[13px]">
        {{ text }}
        <img :src="icon" alt="icon" class="ml-[76px] mr-[28px]">
    </button>
</template>