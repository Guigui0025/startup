<template>
  <nav class="sticky top-0">
    <div
      class="flex items-center justify-between flex-wrap bg-[#fcfcfc] h-20 px-4 border-b border-white"
    >
      <div class="flex items-center">
        <nuxt-link to="/">
          <slot name="logo"></slot>
        </nuxt-link>
      </div>

      <ul class="hidden md:flex items-center justify-end space-x-8 flex-1">
        <slot name="links"></slot>
      </ul>

      <ul class="flex">
        <li class="md:hidden">
          <button @click="isOpen = !isOpen">
            <i v-if="!isOpen" class="ri-menu-line text-3xl"></i>
            <i v-else class="ri-close-line text-3xl"></i>
          </button>
        </li>
      </ul>
    </div>

    <ul
      v-show="isOpen"
      class="md:hidden flex flex-col space-y-2 px-4 py-8 border-b border-white bg-gray-900"
    >
      <slot name="links"></slot>
    </ul>
  </nav>
</template>

<script setup>
import { ref } from "vue";

const isOpen = ref(false);
</script>
