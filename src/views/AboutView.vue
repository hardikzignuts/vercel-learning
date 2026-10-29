<script setup>
const envLabel = import.meta.env.VITE_ENV_LABEL || 'Local'
const apiUrl = import.meta.env.VITE_API_BASE_URL
</script>

<template>
  <div class="about">
    <h1>This is an about page</h1>
    <div v-if="envLabel !== 'Production'" class="env-badge">
    {{ envLabel }} · API: {{ apiUrl }}
  </div>
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
