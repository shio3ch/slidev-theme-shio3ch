<template>
  <div class="slidev-layout cover-layout">
    <div class="cover-content">
      <slot />
    </div>
  </div>
</template>

<style>
.slidev-layout {
  background-color: #0f172a;
  color: #e2e8f0;
}
.cover-layout {
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 4rem;
}
.cover-content {
  text-align: center;
  font-size: 2.5rem;
  color: #2f6fed;
}
</style>
