<script setup>
const props = defineProps({
  icon: {
    type: String,
  },
  text: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <button
    class="flex items-center text-nowrap py-[13px] pl-[26px] rounded-[6px]"
  >
    {{ text }}
    <img v-if="icon" :src="icon" alt="icon" class="mr-[24px] ml-[44px]" />
  </button>
</template>
