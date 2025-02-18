<script setup>
import LogoComponent from '@/components/custom/LogoComponent.vue'
import { navlinks } from '@/lib/navlinks.js'
</script>

<template>
    <div class="flex items-center border mt-[40px] mb-[10px]">
        <div class="mr-[266px]">
            <logo-component />
        </div>

        <div class="flex items-center">
            <nav v-for="links in navlinks" :key="links.text">
                <nuxt-link :to="links.route" class="mr-[36px] text-green text-[16px]">{{ links.text }}</nuxt-link>
            </nav>
        </div>
    </div>
</template>