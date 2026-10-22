<script setup lang="ts">
defineProps<{
  src: string
  alt?: string
}>()
</script>

<template>
  <div class="profile-avatar">
    <span class="avatar-frame">
      <img
        :src="src"
        :alt="alt ?? ''"
        oncontextmenu="return false;"
        ondragstart="return false;"
      />
    </span>
  </div>
</template>

<style scoped>
.profile-avatar {
  display: block;
  line-height: 0;
  max-width: 100%;
  position: relative;
  text-align: center;
  margin-bottom: 2rem;
}

.avatar-frame {
  width: 7.5rem;
  height: 7.5rem;
  aspect-ratio: 1 / 1;
  border-radius: 50%;
  border: 1px solid rgba(255, 255, 255, 0.569);
  display: inline-block;
  overflow: hidden;
  vertical-align: top;
  box-sizing: border-box;
}

.avatar-frame img {
  width: 100%;
  height: 100%;
  aspect-ratio: 1 / 1;
  object-fit: cover;
  object-position: center;
  border-radius: 50%;
  padding: 0.375rem;
  display: block;
  box-sizing: border-box;
  user-select: none;
  -webkit-touch-callout: none;
  transition: transform 0.25s ease, filter 0.25s ease;
}

.avatar-frame:hover img {
  transform: scale(1.05);
}

@media (max-width: 360px) {
  .avatar-frame {
    width: 6.5625rem;
    height: 6.5625rem;
  }
}
</style>

