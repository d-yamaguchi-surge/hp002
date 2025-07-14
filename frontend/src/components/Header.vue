<template>
  <header class="flex justify-between items-center p-4 bg-white relative z-50">
    <div class="text-2xl font-bold text-apaiser-green">
      apaiser
    </div>
    <button 
      @click="$emit('toggle-menu')"
      class="flex flex-col justify-center items-center w-8 h-8 space-y-1"
      aria-label="メニューを開く"
    >
      <span class="w-6 h-0.5 bg-apaiser-green transition-all duration-300"></span>
      <span class="w-6 h-0.5 bg-apaiser-green transition-all duration-300"></span>
      <span class="w-6 h-0.5 bg-apaiser-green transition-all duration-300"></span>
    </button>
  </header>
</template>

<script setup lang="ts">
defineEmits<{
  'toggle-menu': []
}>()
</script>
