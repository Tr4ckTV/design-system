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
    class="transform rounded-xl h-40 w-40 sm:h-64 sm:w-64 bg-gray-700 shadow-xl transition duration-300 hover:scale-105 flex flex-col p-4 group hover:bg-gray-200/75 transition items-center justify-center ring-2 ring-gray-200/75 my-8 space-y-2"
  >
    <div class="text-5xl text-gray-400 group-hover:text-gray-800 transition">
      <slot name="icon" />
    </div>

    <div class="text-xl text-gray-100 group-hover:text-black transition">
      <slot />
    </div>
  </NuxtLink>
</template>
