<script setup>
import { ref } from 'vue'
import { RouterLink, useRoute } from 'vue-router'

const isOpen = ref(false)
const route = useRoute()

const navItems = [
  { name: 'Home', to: '/' },
  { name: 'Portfolio', to: '/portfolio' },
  { name: 'About', to: '/about' },
  { name: 'Contact', to: '/contact' },
]
</script>

<template>
  <header class="sticky top-0 z-40 w-full border-b border-gray-200 bg-white/80 backdrop-blur">
    <nav class="mx-auto flex max-w-7xl items-center justify-between px-4 py-3 md:py-4">
      <RouterLink to="/" class="flex items-center gap-2">
        <span class="inline-block h-8 w-8 rounded bg-brand"></span>
        <span class="font-display text-xl font-semibold tracking-tight">Aurora Studio</span>
      </RouterLink>

      <button class="inline-flex items-center justify-center rounded-md p-2 text-gray-700 md:hidden" @click="isOpen = !isOpen" aria-label="Toggle menu">
        <svg v-if="!isOpen" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="h-6 w-6">
          <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
        </svg>
        <svg v-else xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="h-6 w-6">
          <path stroke-linecap="round" stroke-linejoin="round" d="M6 18 18 6M6 6l12 12" />
        </svg>
      </button>

      <ul class="hidden items-center gap-8 md:flex">
        <li v-for="item in navItems" :key="item.to">
          <RouterLink :to="item.to" class="text-sm font-medium hover:text-brand" :class="{ 'text-brand': route.path === item.to }">{{ item.name }}</RouterLink>
        </li>
      </ul>
    </nav>
    <transition name="fade">
      <div v-if="isOpen" class="border-t border-gray-200 bg-white md:hidden">
        <ul class="mx-auto max-w-7xl px-4 py-3">
          <li v-for="item in navItems" :key="item.to" class="py-2">
            <RouterLink :to="item.to" class="block text-base font-medium" :class="{ 'text-brand': route.path === item.to }" @click="isOpen = false">{{ item.name }}</RouterLink>
          </li>
        </ul>
      </div>
    </transition>
  </header>
</template>

<style scoped>
.fade-enter-active, .fade-leave-active { transition: opacity .15s ease; }
.fade-enter-from, .fade-leave-to { opacity: 0; }
</style>