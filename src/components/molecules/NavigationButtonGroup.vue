<script setup lang="ts">
import ActionButton from '../atoms/ActionButton.vue'

export interface NavButton {
  label: string
  icon: string
  href?: string
  target?: string
  rel?: string
  action?: string
}

defineProps<{
  buttons: NavButton[]
}>()

const emit = defineEmits<(e: 'navigate', action: string) => void>()

function onButtonClick(btn: NavButton, event: MouseEvent) {
  if (btn.action) {
    event.preventDefault()
    emit('navigate', btn.action)
  }
}
</script>

<template>
  <nav class="nav-button-group">
    <ul class="button-list">
      <li
        v-for="(btn, index) in buttons"
        :key="btn.label"
        class="button-item"
        :style="{ animationDelay: `${0.24 + index * 0.08}s` }"
      >
        <ActionButton
          :label="btn.label"
          :icon="btn.icon"
          :href="btn.href"
          :target="btn.target"
          :rel="btn.rel"
          @click="onButtonClick(btn, $event)"
        />
      </li>
    </ul>
  </nav>
</template>

<style scoped>
.nav-button-group {
  margin-top: 2rem;
  width: 24rem;
  max-width: 100%;
  background-image: linear-gradient(45deg, rgba(0, 0, 0, 0.078) 0%, rgba(0, 0, 0, 0.271) 100%);
  background-position: 0% 0%;
  background-repeat: repeat;
  background-size: cover;
  -webkit-backdrop-filter: blur(0.3rem);
  backdrop-filter: blur(0.3rem);
  border: 1px solid rgba(255, 255, 255, 0.271);
  border-radius: 1.25rem;
  padding: 2rem;
  box-sizing: border-box;
  animation: fadeUp 0.8s cubic-bezier(0.16, 1, 0.3, 1) 0.15s both;
}

.button-list {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
  flex-direction: column;
  gap: 1.25rem;
  width: 100%;
}

.button-item {
  width: 100%;
  animation: fadeUp 0.8s cubic-bezier(0.16, 1, 0.3, 1) both;
}

@keyframes fadeUp {
  0% {
    opacity: 0;
    transform: translateY(1.5rem);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

@media (max-width: 480px) {
  .nav-button-group {
    width: 100%;
    padding: 1.5rem 1.25rem;
  }
}

@media (max-width: 360px) {
  .nav-button-group {
    padding: 1.25rem 1rem;
  }

  .button-list {
    gap: 0.9375rem;
  }
}
</style>

