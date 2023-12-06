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
    active-class="text-red-500"
    class="menu-link hover:text-red-500"
  >
    <slot />
    <span
      class="menu absolute bottom-0 left-0 right-0 block w-0 h-1"
      style="content: '.'"
    ></span>
  </NuxtLink>
</template>

<style scoped>
.menu-link {
  position: relative;
}

.menu-link:after,
.menu-link:before {
  content: "";
  position: absolute;
  display: block;
  border: 0px solid transparent;
  width: 0%;
  height: 0%;
  transition: all 0.3s ease;
}

.menu-link:after {
  width: 0%;
  height: 0%;
  border-top: 2px solid transparent;
  border-left: 2px solid transparent;
  top: -5px;
  left: -10px;
}

.menu-link:before {
  width: 0%;
  height: 0%;
  right: -10px;
  bottom: -5px;
  border-bottom: 2px solid transparent;
  border-right: 2px solid transparent;
}

.menu-link:hover::before,
.menu-link:hover::after {
  width: 10px;
  height: 10px;
  border-color: #ef4444;
}
</style>
