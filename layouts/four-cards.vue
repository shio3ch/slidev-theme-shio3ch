<script setup lang="ts">
</script>

<template>
  <div class="slidev-layout four-cards">
    <div class="four-cards-header">
      <slot name="header" />
    </div>
    <div class="four-cards-grid">
      <div class="four-cards-cell">
        <slot name="one" />
      </div>
      <div class="four-cards-cell">
        <slot name="two" />
      </div>
      <div class="four-cards-cell">
        <slot name="three" />
      </div>
      <div class="four-cards-cell">
        <slot name="four" />
      </div>
    </div>
  </div>
</template>
