<template>
  <div class="min-h-screen bg-white">
    <Header @toggle-menu="toggleMenu" />
    <MobileMenu :is-open="isMenuOpen" @close="closeMenu" />
    <HeroSection />
    <ConceptSection />
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import Header from '@/components/Header.vue'
import MobileMenu from '@/components/MobileMenu.vue'
import HeroSection from '@/components/HeroSection.vue'
import ConceptSection from '@/components/ConceptSection.vue'

const isMenuOpen = ref(false)

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value
}

const closeMenu = () => {
  isMenuOpen.value = false
}
</script>
