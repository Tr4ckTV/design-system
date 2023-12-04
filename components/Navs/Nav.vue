<template>
  <nav
    class="flex items-center justify-between flex-wrap bg-pink-200 h-20 px-4 border-b border-white text-cyan-500"
  >
    <div>
      <nuxt-link to="/" class="text-cyan-500 text-2xl font-bold">
        <slot name="logo">Logo</slot>
      </nuxt-link>
    </div>
    <ul class="flex items-center justify-between space-x-8">
      <slot name="links"></slot>
    </ul>
  </nav>
</template>
