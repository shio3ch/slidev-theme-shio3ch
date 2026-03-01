<script setup lang="ts">
</script>

<template>
  <div class="slidev-layout cards">
    <div class="cards-header">
      <slot />
    </div>
    <div class="cards-grid">
      <div class="card">
        <slot name="one" />
      </div>
      <div class="card">
        <slot name="two" />
      </div>
      <div class="card">
        <slot name="three" />
      </div>
    </div>
  </div>
</template>
