<template>
  <div 
    class="fixed top-0 left-0 w-full bg-white shadow-lg transform transition-transform duration-300 ease-in-out z-40"
    :class="isOpen ? 'translate-y-0' : '-translate-y-full'"
  >
    <div class="pt-20 pb-6">
      <nav class="flex flex-col">
        <a 
          href="#" 
          class="px-6 py-4 text-lg font-medium text-gray-800 hover:bg-gray-50 hover:text-apaiser-green transition-colors"
          @click="$emit('close')"
        >
          TOP
        </a>
        <a 
          href="#" 
          class="px-6 py-4 text-lg font-medium text-gray-800 hover:bg-gray-50 hover:text-apaiser-green transition-colors"
          @click="$emit('close')"
        >
          MENU
        </a>
        <a 
          href="#" 
          class="px-6 py-4 text-lg font-medium text-gray-800 hover:bg-gray-50 hover:text-apaiser-green transition-colors"
          @click="$emit('close')"
        >
          ABOUT
        </a>
        <a 
          href="#" 
          class="px-6 py-4 text-lg font-medium text-gray-800 hover:bg-gray-50 hover:text-apaiser-green transition-colors"
          @click="$emit('close')"
        >
          CONTACT
        </a>
      </nav>
    </div>
  </div>
</template>

<script setup lang="ts">
defineProps<{
  isOpen: boolean
}>()

defineEmits<{
  close: []
}>()
</script>
