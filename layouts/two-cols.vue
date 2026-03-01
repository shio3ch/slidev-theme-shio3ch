<script setup lang="ts">
</script>

<template>
  <div class="slidev-layout two-cols" :class="{ 'has-header': $slots.header }">
    <div v-if="$slots.header" class="col-header">
      <slot name="header" />
    </div>
    <div class="col-left">
      <slot name="left">
        <slot />
      </slot>
    </div>
    <div class="col-right">
      <slot name="right" />
    </div>
  </div>
</template>
