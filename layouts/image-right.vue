<script setup lang="ts">
defineProps<{
  image: string
}>()
</script>

<template>
  <div class="slidev-layout image-right">
    <div class="image-right-content">
      <slot />
    </div>
    <div
      class="image-right-image"
      :style="{ backgroundImage: `url(${image})` }"
    />
  </div>
</template>
