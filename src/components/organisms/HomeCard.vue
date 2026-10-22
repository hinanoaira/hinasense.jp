<script setup lang="ts">
import ProfileAvatar from '../atoms/ProfileAvatar.vue'
import NavigationButtonGroup, { type NavButton } from '../molecules/NavigationButtonGroup.vue'
import ProfileBio from '../molecules/ProfileBio.vue'
import SocialButtonGroup, { type SocialLink } from '../molecules/SocialButtonGroup.vue'

const emit = defineEmits<(e: 'navigate', action: string) => void>()

const navButtons: NavButton[] = [
  {
    label: '雛野あいらとは？',
    icon: 'icon-5df67a211ae41c4e5f96b6e0ea004ca3',
    action: 'about',
  },
  {
    label: 'にりらみすきー部',
    icon: 'icon-01bb634a2bbaa3d60414aca70c40f474',
    href: 'https://misskey.niri.la/@hinanoaira',
    target: '_blank',
    rel: 'me',
  },
  {
    label: '隠れ家',
    icon: 'icon-01bb634a2bbaa3d60414aca70c40f474',
    href: 'https://misskey.yukineko.me/@hinanoaira',
    target: '_blank',
    rel: 'me',
  },
  {
    label: 'VRChat',
    icon: 'icon-1db0d045f9177cd3dc2399af17843596',
    href: 'https://vrchat.com/home/user/usr_34a26ee1-7b28-4a01-9643-0cc5e4fbf8a4',
    target: '_blank',
    rel: 'me',
  },
  {
    label: 'ほしいものリスト',
    icon: 'icon-087398ed0fe899085b907a25f76573d4',
    href: 'https://booth.pm/wish_list_names/KAaTWYD1',
    target: '_blank',
  },
]

const socialLinks: SocialLink[] = [
  {
    name: 'Discord',
    icon: 'icon-3b7eeeccbb457780f277fce4669f67a0',
    href: 'https://discord.gg/ErXXnSDxcf',
  },
  {
    name: 'GitHub',
    icon: 'icon-8c4b37645de3c276d895d87df51ba614',
    href: 'https://github.com/hinanoaira',
  },
  {
    name: 'X',
    icon: 'icon-31b8880d36499db40d4e47546c4763f3',
    href: 'https://x.com/hinanoaira',
  },
]
</script>

<template>
  <div class="home-card">
    <ProfileAvatar
      src="/assets/images/image01.jpg"
      alt="雛野あいら"
      class="home-avatar"
    />
    <ProfileBio
      name="雛野あいら"
      tagline="ねこでありたい"
      class="home-bio"
    />
    <NavigationButtonGroup
      :buttons="navButtons"
      @navigate="emit('navigate', $event)"
    />
    <SocialButtonGroup
      :links="socialLinks"
    />
  </div>
</template>

<style scoped>
.home-card {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.home-avatar {
  animation: fadeUp 0.8s cubic-bezier(0.16, 1, 0.3, 1) 0s both;
}

.home-bio {
  animation: fadeUp 0.8s cubic-bezier(0.16, 1, 0.3, 1) 0.1s both;
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
</style>

