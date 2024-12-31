<script setup lang="ts">
import Header from './components/Header.vue'
import Sidebar from './components/Sidebar.vue'
import VideoGrid from './components/VideoGrid.vue'
</script>

<template>
  <div class="min-h-screen bg-gray-50">
    <Header />
    <Sidebar />
    <main class="ml-64 pt-14">
      <VideoGrid />
    </main>
  </div>
</template>