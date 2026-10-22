<script setup lang="ts">
defineProps<{
  name: string
  title?: string
}>()
</script>

<template>
  <svg aria-hidden="true" class="svg-icon">
    <title v-if="title">{{ title }}</title>
    <use :href="`#${name}`"></use>
  </svg>
</template>

<style scoped>
.svg-icon {
  display: block;
  fill: currentColor;
  pointer-events: none;
}
</style>

