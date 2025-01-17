<template>
  <span v-for="a in message">{{ a }}</span>
</template>

<script setup lang="ts">
const props = defineProps<{
  message: string
}>()
</script>
