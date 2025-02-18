<script setup>
import LogoComponent from '@/components/custom/LogoComponent.vue'
import { navlinks } from '@/lib/navlinks.js'
</script>

<template>
    <div class="border mt-[40px] mb-[10px]">
        <div>
            <logo-component />
        </div>

        <div>
            <nav v-for="links in navlinks" :key="links.text">
                <nuxt-link :to="links.route">{{ links.text }}</nuxt-link>
            </nav>
        </div>
    </div>
</template>