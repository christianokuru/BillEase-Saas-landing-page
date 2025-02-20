<script setup>
const props = defineProps({
  text: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <button class="text-nowrap py-[10px] px-[26px] rounded-[8px]">
    {{ text }}
    <slot />
  </button>
</template>
