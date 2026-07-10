<script setup lang="ts">
import { nextTick, onBeforeUnmount, onMounted } from 'vue'
import { RouterView } from 'vue-router'

import AppFooter from '@/components/layout/AppFooter.vue'
import AppHeader from '@/components/layout/AppHeader.vue'

let observer: IntersectionObserver | null = null

onMounted(async () => {
  await nextTick()

  observer = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (!entry.isIntersecting) return

        entry.target.classList.add('fade-in')
        entry.target.classList.remove('opacity-0')
        observer?.unobserve(entry.target)
      })
    },
    {
      threshold: 0.1,
    },
  )

  document.querySelectorAll<HTMLElement>('main section').forEach((section) => {
    if (section.id === 'hero') {
      section.classList.add('fade-in')
      return
    }

    section.classList.add('opacity-0')
    observer?.observe(section)
  })
})

onBeforeUnmount(() => {
  observer?.disconnect()
})
</script>

<template>
  <div id="app" class="flex min-h-screen flex-col pb-20 md:pb-0">
    <AppHeader />
    <RouterView />
    <AppFooter />
  </div>
</template>
