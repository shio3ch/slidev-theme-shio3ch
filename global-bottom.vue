<script setup lang="ts">
import { computed } from 'vue'
import { useNav } from '@slidev/client'

import mascotImage from './public/kappa.png'

const { currentLayout } = useNav()

// マスコットを非表示にするレイアウト
const hiddenLayouts = ['cover', 'intro', 'section', 'fact', 'statement', 'quote', 'center', 'end']

const showMascot = computed(() => {
  return !hiddenLayouts.includes(currentLayout.value ?? '')
})
</script>

<template>
  <div v-if="showMascot" class="mascot-container">
    <img :src="mascotImage" alt="mascot" class="mascot" />
  </div>
</template>

<style scoped>
.mascot-container {
  position: fixed;
  bottom: 1rem;
  right: 1rem;
  z-index: 10;
  pointer-events: none;
}

.mascot {
  width: 80px;
  height: auto;
  opacity: 0.4;
  transition: opacity 0.3s ease;
}

.mascot-container:hover .mascot {
  opacity: 0.7;
}
</style>
