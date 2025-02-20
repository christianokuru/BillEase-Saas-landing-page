<script setup>
import first from "@/assets/images/1.svg"
import second from "@/assets/images/2.svg"
import third from "@/assets/images/3.svg"
import fourth from "@/assets/images/4.svg"
import fifth from "@/assets/images/5.svg"
import sixth from "@/assets/images/6.svg"

const images = [first, second, third, fourth, fifth, sixth]
</script>

<template>
    <div class="border bg-green mx-[-120px] flex items-center space-x-[79.6px] px-[221px] py-[47.57px] mb-[160px]">
        <div v-for="(image, index) in images" :key="index">
            <div>
                <img :src="image" alt="sponsor-logo" class="space-x-[79.6px] animate-pulse">
            </div>
        </div>
    </div>
</template>