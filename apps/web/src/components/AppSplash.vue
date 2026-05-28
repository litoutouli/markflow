<script setup lang="ts">
import markflowIcon from '@/assets/images/markflow-icon.png'

const loading = ref(true)

onMounted(() => {
  setTimeout(() => {
    loading.value = false
  }, 100)
})
</script>

<template>
  <transition name="fade">
    <div
      v-if="loading"
      class="loading"
    >
      <img class="loading-icon" :src="markflowIcon" alt="" aria-hidden="true">
      <strong>MarkFlow</strong>
    </div>
  </transition>
</template>

<style lang="less" scoped>
.loading {
  position: fixed;
  top: 0;
  left: 0;
  z-index: 99999;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 100vw;
  height: 100vh;
  font-size: 18px;
  background-color: hsl(var(--background));
}

.loading-icon {
  width: 104px;
  height: 104px;
  margin-bottom: 24px;
  object-fit: contain;
  filter: drop-shadow(0 16px 28px rgb(15 23 42 / 0.16));
}

.fade-enter,
.fade-leave-to {
  opacity: 0;
}

.fade-enter-to,
.fade-leave {
  opacity: 1;
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 1s;
}
</style>
