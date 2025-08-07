<script setup>
import { onMounted, onBeforeUnmount } from 'vue'
import PhotoSwipeLightbox from 'photoswipe/lightbox'
import 'photoswipe/style.css'

const images = [
  { src: 'https://images.unsplash.com/photo-1520975940091-6c59fd4e8b72?q=80&w=1600&auto=format&fit=crop', w: 1600, h: 2000, alt: 'Portrait' },
  { src: 'https://images.unsplash.com/photo-1529626455594-4ff0802cfb7e?q=80&w=1600&auto=format&fit=crop', w: 1600, h: 1068, alt: 'Couple' },
  { src: 'https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?q=80&w=1600&auto=format&fit=crop', w: 1600, h: 1067, alt: 'Wedding' },
  { src: 'https://images.unsplash.com/photo-1542037104857-ffbb0b9155fb?q=80&w=1600&auto=format&fit=crop', w: 1600, h: 2000, alt: 'Brand' },
  { src: 'https://images.unsplash.com/photo-1520975588253-9bffb43057ef?q=80&w=1600&auto=format&fit=crop', w: 1600, h: 1067, alt: 'Event' },
  { src: 'https://images.unsplash.com/photo-1544005313-94ddf0286df2?q=80&w=1600&auto=format&fit=crop', w: 1600, h: 1067, alt: 'Smile' },
  { src: 'https://images.unsplash.com/photo-1511285560929-80b456fea0bc?q=80&w=1600&auto=format&fit=crop', w: 1600, h: 1067, alt: 'Studio' },
  { src: 'https://images.unsplash.com/photo-1490902931801-d6f80ca94fe1?q=80&w=1600&auto=format&fit=crop', w: 1600, h: 1067, alt: 'Lifestyle' },
]

let lightbox

onMounted(() => {
  lightbox = new PhotoSwipeLightbox({
    gallery: '#portfolio-gallery',
    children: 'a',
    pswpModule: () => import('photoswipe'),
  })
  lightbox.init()
})

onBeforeUnmount(() => {
  lightbox?.destroy()
})
</script>

<template>
  <section class="mx-auto max-w-7xl px-4 py-12">
    <div class="mb-6 flex items-end justify-between gap-4">
      <div>
        <h1 class="font-display text-3xl font-bold">Portfolio</h1>
        <p class="mt-1 text-gray-600">A curated selection of our recent work.</p>
      </div>
    </div>

    <div id="portfolio-gallery" class="columns-1 gap-4 sm:columns-2 lg:columns-3">
      <a v-for="img in images" :key="img.src" :href="img.src" :data-pswp-width="img.w" :data-pswp-height="img.h" :title="img.alt" class="mb-4 block break-inside-avoid overflow-hidden rounded-lg">
        <img :src="img.src + '&dpr=1'" :alt="img.alt" class="w-full transform object-cover transition duration-300 ease-out hover:scale-[1.02]" loading="lazy" />
      </a>
    </div>
  </section>
</template>