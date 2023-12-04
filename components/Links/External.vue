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
    <span>
      <slot />
    </span>
    <span>
      <i></i>
    </span>
  </NuxtLink>
</template>
