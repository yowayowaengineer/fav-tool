<template>
  <div>
    <div class="test2" v-if="message" v-for="a in message">{{ a }}</div>
    <img class="test" v-if="imgsrc" :src="imgsrc" />
  </div>
</template>

<script setup lang="ts">
const props = defineProps<{
  message: string
  imgsrc: string
}>()
</script>

<style lang="css" scoped>
.test {
  animation: falling 5s 5s forwards;
}
.test2 {
  animation: fallingLeaves 7s 10s forwards;
}

@keyframes falling {
  0% {
    transform: translate3d(300, 0, 0) rotate(0deg);
  }

  100% {
    transform: translate3d(-350px, 700px, 0) rotate(90deg);
    opacity: 0;
  }
}

@keyframes falling3 {
  0% {
    transform: translate3d(0, 0, 0) rotate(-20deg);
  }

  100% {
    transform: translate3d(-230px, 640px, 0) rotate(-70deg);
    opacity: 0;
  }
}

@keyframes falling2 {
  0% {
    transform: translate3d(0, 0, 0) rotate(90deg);
  }

  100% {
    transform: translate3d(-400px, 680px, 0) rotate(0deg);
    opacity: 0;
  }
}

@keyframes fallingLeaves {
  0% {
    opacity: 1;
    -webkit-transform: translate(0, 0px) rotateZ(0deg);
  }
  75% {
    opacity: 1;
    -webkit-transform: translate(100px, 600px) rotateZ(270deg);
  }
  100% {
    opacity: 0;
    -webkit-transform: translate(150px, 800px) rotateZ(360deg);
  }
}
</style>
