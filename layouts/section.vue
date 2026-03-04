<script setup lang="ts">
defineProps<{
  sectionNumber?: string
}>()
</script>

<template>
  <div class="slidev-layout section w-full h-full grid">
    <!-- 装飾: 背景の巨大ナンバー -->
    <div v-if="sectionNumber" class="section-bg-number">{{ sectionNumber }}</div>
    <div class="my-auto text-center">
      <slot />
    </div>
    <!-- 装飾: 下部中央アクセントライン -->
    <div class="section-accent-line" />
  </div>
</template>
