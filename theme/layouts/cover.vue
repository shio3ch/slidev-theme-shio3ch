<script setup lang="ts">
import { computed } from 'vue'
import { handleBackground } from '@slidev/client'

const props = defineProps<{
  background?: string
}>()

const style = computed(() => handleBackground(props.background))
</script>

<template>
  <div class="slidev-layout cover" :style="style">
    <div class="my-auto w-full">
      <slot />
    </div>
  </div>
</template>
