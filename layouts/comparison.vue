<script setup lang="ts">
defineProps<{
  labelLeft?: string
  labelRight?: string
}>()
</script>

<template>
  <div class="slidev-layout comparison">
    <div class="comparison-header">
      <slot name="header" />
    </div>
    <div class="comparison-columns">
      <div class="comparison-col comparison-col-left">
        <div v-if="labelLeft" class="comparison-label">{{ labelLeft }}</div>
        <div class="comparison-content">
          <slot />
        </div>
      </div>
      <div class="comparison-divider" />
      <div class="comparison-col comparison-col-right">
        <div v-if="labelRight" class="comparison-label">{{ labelRight }}</div>
        <div class="comparison-content">
          <slot name="right" />
        </div>
      </div>
    </div>
  </div>
</template>
