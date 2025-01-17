<template>
  <div>
    <span v-if="message" v-for="a in message">{{ a }}</span>
    <img v-if="imgsrc" :src="imgsrc" />
  </div>
</template>

<script setup lang="ts">
const props = defineProps<{
  message: string
  imgsrc: string
}>()
</script>
