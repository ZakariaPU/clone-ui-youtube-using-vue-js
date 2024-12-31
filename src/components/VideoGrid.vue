<script setup lang="ts">
const videos = Array.from({ length: 12 }, (_, i) => ({
  id: i + 1,
  thumbnail: `https://picsum.photos/seed/${i}/320/180`,
  title: `Video Title ${i + 1}`,
  channel: `Channel ${i + 1}`,
  views: Math.floor(Math.random() * 1000000),
  timestamp: '3 days ago'
}))
</script>

<template>
  <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-4 p-4">
    <div v-for="video in videos" :key="video.id" class="cursor-pointer">
      <div class="relative">
        <img :src="video.thumbnail" alt="Video thumbnail" class="w-full rounded-lg" />
        <span class="absolute bottom-2 right-2 bg-black bg-opacity-80 text-white text-xs px-2 py-1 rounded">
          8:24
        </span>
      </div>
      <div class="mt-2 flex">
        <div class="flex-shrink-0">
          <div class="w-9 h-9 rounded-full bg-gray-200"></div>
        </div>
        <div class="ml-3">
          <h3 class="text-sm font-semibold line-clamp-2">{{ video.title }}</h3>
          <p class="text-sm text-gray-600 mt-1">{{ video.channel }}</p>
          <p class="text-sm text-gray-600">
            {{ video.views.toLocaleString() }} views • {{ video.timestamp }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>