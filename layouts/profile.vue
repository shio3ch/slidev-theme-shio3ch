<script setup lang="ts">
defineProps<{
  image?: string
}>()
</script>

<template>
  <div class="slidev-layout profile">
    <div class="profile-top">
      <div v-if="image" class="profile-avatar">
        <img :src="image" alt="avatar" />
      </div>
      <div class="profile-name">
        <slot name="name" />
      </div>
    </div>
    <div class="profile-body">
      <slot />
    </div>
  </div>
</template>
