<template>
  <div class="title" style="--duration: 1s">
    <span style="--delay: 0.5s">{{ message }}</span>
  </div>
</template>

<script setup lang="ts">
const props = defineProps<{
  message: string
  backgroundColor: string
}>()
</script>

<style lang="css" scoped>
.title span {
  --total: calc(var(--duration) + var(--delay));
  position: relative;
  display: block;
  color: transparent;
  overflow: hidden;
  animation: reveal 1s var(--total) forwards;
}
.title span::after {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  transform: scaleX(0);
  transform-origin: left;
  background-image: v-bind(backgroundColor);
  animation:
    rollIn var(--duration) var(--delay) forwards,
    rollOut var(--duration) var(--total) forwards;
}
.title span:nth-child(2)::after {
  border-top: 3px solid #004ab8;
}
@keyframes reveal {
  to {
    color: #000;
  }
}
@keyframes rollIn {
  from {
    transform: scaleX(0);
  }
  to {
    transform: scaleX(1);
  }
}
@keyframes rollOut {
  from {
    transform: translateX(0);
  }
  to {
    transform: translateX(105%);
  }
}
</style>
