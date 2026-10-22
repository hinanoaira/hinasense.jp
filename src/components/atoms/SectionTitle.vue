<script setup lang="ts">
defineProps<{
  title: string
}>()
</script>

<template>
  <h1 class="section-title">{{ title }}</h1>
</template>

<style scoped>
.section-title {
  color: #ffffff;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 2.5em;
  line-height: 1.125;
  font-weight: 700;
  letter-spacing: 0rem;
  width: 100%;
  margin: 1.5rem 0 1rem 0;
  text-align: left;
}

.section-title:first-of-type {
  margin-top: 1rem;
}

@media (max-width: 736px) {
  .section-title {
    font-size: 2.5em;
    margin: 1.25rem 0 0.75rem 0;
  }

  .section-title:first-of-type {
    margin-top: 0.75rem;
  }
}
</style>
