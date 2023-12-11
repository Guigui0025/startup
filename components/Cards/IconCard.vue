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
    class="flex flex-col p-4 group hover:bg-[#222c5f] transition items-center justify-center ring-2 ring-gray-200/75 my-8 space-y-2"
  >
    <div class="text-5xl text-[#222c5f] group-hover:text-[#E75A36] transition">
      <slot name="icon" />
    </div>

    <div
      class="text-xl text-[#222c5f] group-hover:text-[#E75A36] group-hover:underline transition"
    >
      <slot />
    </div>
  </NuxtLink>
</template>
