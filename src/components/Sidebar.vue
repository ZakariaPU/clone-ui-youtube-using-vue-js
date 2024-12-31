<script setup lang="ts">
import { HomeIcon, FireIcon, ClockIcon, FilmIcon, BookmarkIcon } from '@heroicons/vue/24/outline'

const menuItems = [
  { icon: HomeIcon, text: 'Home' },
  { icon: FireIcon, text: 'Trending' },
  { icon: ClockIcon, text: 'History' },
  { icon: FilmIcon, text: 'Subscriptions' },
  { icon: BookmarkIcon, text: 'Library' },
]
</script>

<template>
  <aside class="fixed left-0 top-14 h-full w-64 bg-white border-r border-gray-200 overflow-y-auto">
    <nav class="py-4">
      <ul>
        <li v-for="(item, index) in menuItems" :key="index">
          <a href="#" class="flex items-center px-6 py-3 hover:bg-gray-100">
            <component :is="item.icon" class="h-6 w-6 text-gray-600" />
            <span class="ml-4 text-sm">{{ item.text }}</span>
          </a>
        </li>
      </ul>
    </nav>
  </aside>
</template>