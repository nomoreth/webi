<script setup>
import { RouterLink } from 'vue-router'
</script>

<template>
  <section class="relative overflow-hidden">
    <div class="pointer-events-none absolute inset-0 -z-10 bg-gradient-to-b from-brand/10 to-transparent"></div>
    <div class="mx-auto max-w-7xl px-4 py-16 md:py-24">
      <div class="grid items-center gap-10 md:grid-cols-2">
        <div>
          <h1 class="font-display text-4xl font-bold tracking-tight md:text-5xl">Elevate your moments with Aurora Studio</h1>
          <p class="mt-4 text-lg text-gray-600">Professional photography for weddings, portraits, brands, and events. Crafted with light, delivered with heart.</p>
          <div class="mt-6 flex items-center gap-4">
            <RouterLink to="/portfolio" class="rounded-md bg-brand px-6 py-3 text-white shadow hover:bg-brand-dark">View Portfolio</RouterLink>
            <RouterLink to="/contact" class="rounded-md border border-gray-300 px-6 py-3 hover:border-brand">Book a Session</RouterLink>
          </div>
        </div>
        <div class="grid grid-cols-3 grid-rows-3 gap-3 md:gap-4">
          <img class="col-span-2 row-span-2 h-48 w-full rounded-lg object-cover md:h-64" src="https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?q=80&w=1200&auto=format&fit=crop" alt="Wedding" />
          <img class="h-48 w-full rounded-lg object-cover md:h-64" src="https://images.unsplash.com/photo-1520975940091-6c59fd4e8b72?q=80&w=1200&auto=format&fit=crop" alt="Portrait" />
          <img class="h-48 w-full rounded-lg object-cover md:h-64" src="https://images.unsplash.com/photo-1542037104857-ffbb0b9155fb?q=80&w=1200&auto=format&fit=crop" alt="Brand" />
          <img class="col-span-3 h-48 w-full rounded-lg object-cover md:h-64" src="https://images.unsplash.com/photo-1529626455594-4ff0802cfb7e?q=80&w=1600&auto=format&fit=crop" alt="Couple" />
        </div>
      </div>
    </div>
  </section>

  <section class="mx-auto max-w-7xl px-4 py-12">
    <h2 class="font-display text-2xl font-semibold">Featured Services</h2>
    <div class="mt-6 grid gap-6 md:grid-cols-3">
      <div class="rounded-lg border p-6">
        <h3 class="text-lg font-semibold">Weddings</h3>
        <p class="mt-2 text-gray-600">Full-day coverage, storytelling, and album design.</p>
      </div>
      <div class="rounded-lg border p-6">
        <h3 class="text-lg font-semibold">Portraits</h3>
        <p class="mt-2 text-gray-600">Studio and on-location sessions with creative direction.</p>
      </div>
      <div class="rounded-lg border p-6">
        <h3 class="text-lg font-semibold">Commercial</h3>
        <p class="mt-2 text-gray-600">Brand, product, and lifestyle content for campaigns.</p>
      </div>
    </div>
  </section>
</template>