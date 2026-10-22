<script setup lang="ts">
import IconButton from '../atoms/IconButton.vue'

export interface SocialLink {
  name: string
  icon: string
  href: string
}

defineProps<{
  links: SocialLink[]
}>()
</script>

<template>
  <ul class="social-button-group">
    <li
      v-for="(link, index) in links"
      :key="link.name"
      class="social-item"
      :style="{ animationDelay: `${0.64 + index * 0.08}s` }"
    >
      <IconButton
        :name="link.name"
        :icon="link.icon"
        :href="link.href"
      />
    </li>
  </ul>
</template>

<style scoped>
.social-button-group {
  list-style: none;
  padding: 0;
  margin: 1.5rem 0;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  gap: 1.625rem;
}

.social-item {
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

@media (max-width: 360px) {
  .social-button-group {
    gap: 1.21875rem;
  }
}
</style>

