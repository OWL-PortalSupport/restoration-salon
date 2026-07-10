<script setup lang="ts">
import { onBeforeUnmount, onMounted, ref } from 'vue'

const isScrolled = ref(false)
const activeSection = ref('hero')

const navItems = [
  { label: 'Top', href: '#hero', id: 'hero' },
  { label: 'Flow', href: '#flow', id: 'flow' },
  { label: 'Menu', href: '#menu', id: 'menu' },
  { label: 'Access', href: '#access', id: 'access' },
]

const handleScroll = () => {
  isScrolled.value = window.scrollY > 50

  const sections = document.querySelectorAll<HTMLElement>('section')
  let current = 'hero'

  sections.forEach((section) => {
    const sectionTop = section.offsetTop - 120
    const sectionBottom = sectionTop + section.offsetHeight

    if (window.scrollY >= sectionTop && window.scrollY < sectionBottom) {
      current = section.id
    }
  })

  activeSection.value = current
}

onMounted(() => {
  handleScroll()
  window.addEventListener('scroll', handleScroll)
})

onBeforeUnmount(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>

<template>
  <header
    class="fixed top-0 z-50 h-20 w-full bg-surface/90 backdrop-blur-md transition-all duration-300"
    :class="isScrolled ? 'h-16 shadow-sm' : 'h-20'"
  >
    <div class="flex justify-between items-center w-full px-gutter max-w-[1140px] mx-auto h-full">
      <a href="#hero" class="font-headline-md text-2xl font-bold text-primary">
        Restoration Salon
      </a>

      <nav class="hidden items-center gap-margin md:flex">
        <a
          v-for="item in navItems"
          :key="item.id"
          :href="item.href"
          class="nav-link font-label-md text-label-md transition-colors hover:text-primary"
          :class="
            activeSection === item.id
              ? 'border-b-2 border-primary pb-1 font-bold text-primary'
              : 'text-on-surface-variant'
          "
        >
          {{ item.label }}
        </a>
      </nav>
    </div>
  </header>
</template>
