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
    <!-- 装飾: 左上アクセントライン -->
    <div class="cover-accent-line" />
    <!-- 装飾: 右下ジオメトリック矩形 -->
    <div class="cover-geo-rect cover-geo-rect-1" />
    <div class="cover-geo-rect cover-geo-rect-2" />
    <div class="my-auto w-full">
      <slot />
    </div>
  </div>
</template>
