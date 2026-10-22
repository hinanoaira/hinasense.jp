<script setup lang="ts">
defineProps<{
  name: string
  tagline: string
}>()
</script>

<template>
  <div class="profile-bio">
    <h1 class="bio-name">{{ name }}</h1>
    <p class="bio-tagline">{{ tagline }}</p>
  </div>
</template>

<style scoped>
.profile-bio {
  text-align: center;
  margin-top: 0;
  width: 100%;
}

.bio-name {
  color: #ffffff;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 3.5em;
  line-height: 0.75;
  font-weight: 700;
  letter-spacing: 0rem;
  margin: 0;
}

.bio-tagline {
  color: #ffffff;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 1em;
  line-height: 1.875;
  font-weight: 400;
  letter-spacing: 0rem;
  margin-top: 1.25rem;
}

@media (max-width: 736px) {
  .bio-name {
    font-size: 2.5em;
  }
}
</style>
