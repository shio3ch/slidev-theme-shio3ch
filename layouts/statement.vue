<template>
  <div class="slidev-layout statement">
    <!-- 装飾: 上部グラデーションバー -->
    <div class="statement-accent-bar statement-accent-bar-top" />
    <div class="my-auto">
      <slot />
    </div>
    <!-- 装飾: 下部グラデーションバー -->
    <div class="statement-accent-bar statement-accent-bar-bottom" />
  </div>
</template>
