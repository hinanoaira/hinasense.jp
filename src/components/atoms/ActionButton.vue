<script setup lang="ts">
import SvgIcon from './SvgIcon.vue'

defineProps<{
  label: string
  icon?: string
  href?: string
  target?: string
  rel?: string
}>()

const emit = defineEmits<(e: 'click', event: MouseEvent) => void>()

function handleClick(event: MouseEvent) {
  emit('click', event)
}
</script>

<template>
  <a
    :href="href ?? '#'"
    :target="target"
    :rel="rel"
    class="action-button"
    role="button"
    @click="handleClick"
  >
    <SvgIcon v-if="icon" :name="icon" :title="label" class="btn-icon" />
    <span class="btn-label">{{ label }}</span>
  </a>
</template>

<style scoped>
.action-button {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  max-width: 100%;
  height: 3.5rem;
  line-height: calc(3.5rem - 2px);
  padding: 0 1.75rem;
  box-sizing: border-box;
  text-decoration: none;
  white-space: nowrap;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
  font-size: 1em;
  font-weight: 400;
  border-radius: 0.625rem;
  border: 1px solid rgba(255, 255, 255, 0.369);
  background-color: rgba(255, 255, 255, 0.071);
  color: #ffffff;
  background-image: linear-gradient(221deg, rgba(255, 255, 255, 0.122) 3%, transparent 96%);
  background-position: 0% 0%;
  background-repeat: repeat;
  background-size: cover;
  cursor: pointer;
  transition: transform 0.25s ease, color 0.25s ease, background-color 0.25s ease, border-color 0.25s ease;
}

.action-button:hover {
  background-color: rgba(255, 255, 255, 0.15);
  border-color: rgba(255, 255, 255, 0.6);
  transform: translateY(-2px);
}

.btn-icon {
  width: 1.5em;
  height: 100%;
  flex-shrink: 0;
  fill: #ffffff;
  margin-left: -0.125em;
  margin-right: 0.5em;
}

.btn-label {
  overflow: hidden;
  text-overflow: ellipsis;
}
</style>

