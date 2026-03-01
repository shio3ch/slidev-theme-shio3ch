<script setup lang="ts">
defineProps<{
  image: string
}>()
</script>

<template>
  <div class="slidev-layout image-left">
    <div
      class="image-left-image"
      :style="{ backgroundImage: `url(${image})` }"
    />
    <div class="image-left-content">
      <slot />
    </div>
  </div>
</template>
