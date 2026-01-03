<script setup>
</script>

<template>
  <div class="app-container">
    <main class="content">
      <router-view v-slot="{ Component }">
        <transition name="fade" mode="out-in">
          <component :is="Component" />
        </transition>
      </router-view>
    </main>
  </div>
</template>

<style scoped>
.app-container {
  min-height: 100vh;
  font-family: 'Inter', sans-serif;
  background: linear-gradient(135deg, #1e1e2f 0%, #2a2a40 100%);
  color: #fff;
}

.content {
  width: 100%;
  padding: 2rem;
  box-sizing: border-box;
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.3s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>
