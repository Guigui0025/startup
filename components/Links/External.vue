<script setup>
defineProps({
  to: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <NuxtLink
    :to="to"
    target="_blank"
    class="group inline-flex space-x-1.5 items-baseline"
  >
    <span class="underline text-gray-300 group-hover:text-gray-100 transition">
      <slot />
    </span>
    <span>
      <i
        class="ri-external-link-line text-gray-400 group-hover:text-gray-300 transition"
      ></i>
    </span>
  </NuxtLink>
</template>
