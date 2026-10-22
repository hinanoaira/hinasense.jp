<script setup lang="ts">
import SvgIcon from './SvgIcon.vue'

defineProps<{
  name: string
  icon: string
  href: string
}>()
</script>

<template>
  <a
    :href="href"
    :aria-label="name"
    target="_blank"
    rel="me"
    role="button"
    class="icon-button"
  >
    <SvgIcon :name="icon" :title="name" class="icon-svg" />
  </a>
</template>

<style scoped>
.icon-button {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  width: 2em;
  height: 2em;
  border-radius: 50%;
  background-color: rgba(255, 255, 255, 0.11);
  background-image: linear-gradient(221deg, rgba(255, 255, 255, 0.122) 0%, transparent 100%);
  background-position: 0% 0%;
  background-repeat: repeat;
  background-size: cover;
  border: 1px solid rgba(255, 255, 255, 0.369);
  color: #ffffff;
  text-decoration: none;
  font-size: 1.5em;
  box-sizing: border-box;
  cursor: pointer;
  transition: transform 0.25s ease, color 0.25s ease, background-color 0.25s ease, border-color 0.25s ease;
}

.icon-button:hover {
  background-color: rgba(255, 255, 255, 0.22);
  border-color: rgba(255, 255, 255, 0.6);
  transform: translateY(-2px);
}

.icon-svg {
  width: 60%;
  height: 60%;
  fill: #ffffff;
}
</style>

