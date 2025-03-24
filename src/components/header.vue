<template>
  <header class="header" aria-label="En-tête principal">
    <div class="header-container">
      <!-- Logo et titre -->
      <div class="header-left">
        <MusicIcon class="music-icon animate-pulse" />
        <h1 class="header-title">Blind Test</h1>
      </div>
    </div>
  </header>
</template>

<script setup>
import { Music as MusicIcon } from 'lucide-vue-next'
</script>

<style scoped>
.header {
  background-color: #1a1a1a;
  padding: 1rem 0;
  color: white;
}

.header-container {
  display: flex;
  justify-content: center;
  align-items: center;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 1rem;
  border-bottom: 2px solid white;
}

.header-left {
  display: flex;
  align-items: center;
  gap: 1rem;
}

.music-icon {
  width: 32px;
  height: 32px;
  color: white;
}

.header-title {
  font-size: 1.8rem;
  font-weight: bold;
}
</style>