<script setup>
const props = defineProps({
  to: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <NuxtLink
    :to="to"
    class="text-lg text-[#222c5f] hover:text-[#cc3c18] hover:underline transition"
    active-class="font-bold"
  >
    <slot />
  </NuxtLink>
</template>
