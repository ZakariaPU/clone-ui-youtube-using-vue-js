<script setup lang="ts">
import { MagnifyingGlassIcon, VideoCameraIcon, BellIcon, UserCircleIcon } from '@heroicons/vue/24/outline'
</script>

<template>
  <header class="fixed top-0 left-0 right-0 bg-white z-50 flex justify-between items-center px-4 h-14">
    <div class="flex items-center">
      <img src="/youtube-logo.png" alt="YouTube" class="h-5" />
    </div>
    
    <div class="flex items-center flex-grow justify-center max-w-2xl">
      <div class="flex items-center w-full">
        <input
          type="text"
          placeholder="Search"
          class="w-full px-4 py-2 border border-gray-300 rounded-l-full focus:outline-none focus:border-blue-500"
        />
        <button class="px-6 py-2 border border-l-0 border-gray-300 rounded-r-full hover:bg-gray-100">
          <MagnifyingGlassIcon class="h-5 w-5 text-gray-600" />
        </button>
      </div>
    </div>
    
    <div class="flex items-center space-x-4">
      <VideoCameraIcon class="h-6 w-6 text-gray-600 cursor-pointer" />
      <BellIcon class="h-6 w-6 text-gray-600 cursor-pointer" />
      <UserCircleIcon class="h-8 w-8 text-gray-600 cursor-pointer" />
    </div>
  </header>
</template>