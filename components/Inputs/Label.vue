<script setup>
defineProps({
  name: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <label
    :for="name"
    class="block text-sm font-medium text-gray-400 cursor-pointer"
  >
    <slot />
  </label>
</template>
