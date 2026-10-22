<script setup lang="ts">
import { onMounted, onUnmounted, ref } from 'vue'
import AboutCard from './components/organisms/AboutCard.vue'
import AppFooter from './components/organisms/AppFooter.vue'
import HomeCard from './components/organisms/HomeCard.vue'
import SvgIconDefs from './components/organisms/SvgIconDefs.vue'

const currentSection = ref<'home' | 'about'>('home')

function updateSectionFromHash() {
  const hash = window.location.hash.replace(/^#\/?/, '').toLowerCase()
  if (hash === 'about') {
    currentSection.value = 'about'
    document.title = '雛野あいらとは？ - ひなセンス'
  } else {
    currentSection.value = 'home'
    document.title = 'ひなセンス'
  }
  window.scrollTo({ top: 0, behavior: 'instant' })
}

function navigateTo(section: 'home' | 'about') {
  if (section === 'about') {
    window.location.hash = '#about'
  } else {
    window.location.hash = '#home'
  }
}

onMounted(() => {
  updateSectionFromHash()
  window.addEventListener('hashchange', updateSectionFromHash)

  setTimeout(() => {
    document.body.classList.remove('is-loading')
  }, 100)
})

onUnmounted(() => {
  window.removeEventListener('hashchange', updateSectionFromHash)
})
</script>

<template>
  <SvgIconDefs />

  <div class="site-wrapper">
    <main class="site-main">
      <div class="inner">
        <Transition name="fade-slide" mode="out-in">
          <HomeCard
            v-if="currentSection === 'home'"
            key="home"
            @navigate="navigateTo('about')"
          />
          <AboutCard
            v-else-if="currentSection === 'about'"
            key="about"
            @navigate="navigateTo('home')"
          />
        </Transition>

        <AppFooter />
      </div>
    </main>
  </div>
</template>

<style scoped>
.fade-slide-enter-active,
.fade-slide-leave-active {
  transition: opacity 0.35s ease, transform 0.35s ease;
}

.fade-slide-enter-from {
  opacity: 0;
  transform: translateY(1.5rem);
}

.fade-slide-leave-to {
  opacity: 0;
  transform: translateY(-1rem);
}
</style>
