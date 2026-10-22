<script setup lang="ts">
const emit = defineEmits<(e: 'click', event: MouseEvent) => void>()

function onClick(event: MouseEvent) {
  event.preventDefault()
  emit('click', event)
}
</script>

<template>
  <div class="back-link-wrapper">
    <a href="#home" class="back-link" @click="onClick">←Back...</a>
  </div>
</template>

<style scoped>
.back-link-wrapper {
  margin: 1rem 0;
  text-align: left;
  width: 100%;
}

.back-link {
  color: #adadad;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 1.75em;
  line-height: 1.125;
  font-weight: 400;
  letter-spacing: 0rem;
  text-decoration: underline;
  cursor: pointer;
  transition: color 0.25s ease, opacity 0.25s ease;
}

.back-link:hover {
  text-decoration: none;
  color: #ffffff;
}

@media (max-width: 736px) {
  .back-link-wrapper {
    margin: 0.75rem 0;
  }

  .back-link {
    font-size: 1.75em;
  }
}
</style>
