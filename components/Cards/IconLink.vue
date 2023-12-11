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
    class="flex items-baseline space-x-8 p-4 group hover:bg-[#222c5f] transition"
  >
    <div class="text-2xl text-[#222c5f] group-hover:text-[#222c5f] transition">
      <slot name="icon" />
    </div>

    <div
      class="text-lg text-[#222c5f] group-hover:text-black group-hover:underline transition"
    >
      <slot />
    </div>
  </NuxtLink>
</template>
