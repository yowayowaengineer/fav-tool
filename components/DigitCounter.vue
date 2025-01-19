<template>
  <div class="counter-container">
    <div class="space flex" align="center">
      <canvas id="myCanvas" width="88" height="131"></canvas>
      <canvas id="myCanvas2" width="88" height="131"></canvas>
      <canvas id="myCanvas3" width="88" height="131"></canvas>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref, onMounted } from 'vue'

///// constants

const Zero = [1, 1, 1, 0, 1, 1, 1]
const One = [0, 0, 1, 0, 0, 1, 0]
const Two = [1, 0, 1, 1, 1, 0, 1]
const Three = [1, 0, 1, 1, 0, 1, 1]
const Four = [0, 1, 1, 1, 0, 1, 0]
const Five = [1, 1, 0, 1, 0, 1, 1]
const Six = [1, 1, 0, 1, 1, 1, 1]
const Seven = [1, 1, 1, 0, 0, 1, 0]
const Eight = [1, 1, 1, 1, 1, 1, 1]
const Nine = [1, 1, 1, 1, 0, 1, 1]
const OffColor = '#232323'
const OnColor = 'red'

///// data

const currentSpeed = ref(1)

///// mounted

onMounted(() => {
  countDown(300)
})

///// functions

const countDown = (num) => {
  currentSpeed.value = num
  setInterval(decrease, 1000)
}

const decrease = () => {
  if (currentSpeed.value > 0) {
    currentSpeed.value = currentSpeed.value - 1
    drawSpeed(currentSpeed.value)
  } else {
    currentSpeed.value = 0
    drawSpeed(currentSpeed.value)
  }
}

const drawSpeed = (speedValue) => {
  const firstDigit = getFirstDigit(speedValue)
  const secondDigit = getSecondDigit(speedValue)
  const thirdDigit = getThirdDigit(speedValue)

  const c1 = document.getElementById('myCanvas')
  drawNumbers(c1, firstDigit)
  const c2 = document.getElementById('myCanvas2')
  drawNumbers(c2, secondDigit)
  const c3 = document.getElementById('myCanvas3')
  drawNumbers(c3, thirdDigit)
}

const getFirstDigit = (num) => {
  if (num < 100) {
    return Zero
  } else {
    const digit = num.toString()[0]
    switch (digit) {
      case '1':
        return One
      case '2':
        return Two
      case '3':
        return Three
      case '4':
        return Four
      case '5':
        return Five
      case '6':
        return Six
      case '7':
        return Seven
      case '8':
        return Eight
      case '9':
        return Nine
      case '0':
        return Zero
      default:
        return Zero
    }
  }
}

const getSecondDigit = (num) => {
  if (num < 10) {
    return Zero
  } else {
    const digit = (num < 100 ) ? num.toString()[0] : num.toString()[1]
    switch (digit) {
      case '1':
        return One
      case '2':
        return Two
      case '3':
        return Three
      case '4':
        return Four
      case '5':
        return Five
      case '6':
        return Six
      case '7':
        return Seven
      case '8':
        return Eight
      case '9':
        return Nine
      case '0':
        return Zero
      default:
        return Zero
    }
  }
}

const getThirdDigit = (num) => {
  let digit
  if (num < 10) {
    digit = num.toString()[0]
  } else {
    digit = (num < 100 ) ? num.toString()[1] : num.toString()[2]
  }

  switch (digit) {
    case '1':
      return One
    case '2':
      return Two
    case '3':
      return Three
    case '4':
      return Four
    case '5':
      return Five
    case '6':
      return Six
    case '7':
      return Seven
    case '8':
      return Eight
    case '9':
      return Nine
    case '0':
      return Zero
    default:
      return Zero
  }
}

const drawNumbers = (canvas, numberArray) => {
  const topbar = canvas.getContext('2d')
  drawTopBar(topbar, numberArray[0])

  const topleftbar = canvas.getContext('2d')
  drawTopLeftBar(topleftbar, numberArray[1])

  const toprightbar = canvas.getContext('2d')
  drawTopRightBar(toprightbar, numberArray[2])

  const middlebar = canvas.getContext('2d')
  drawMiddleBar(middlebar, numberArray[3])

  const bottomleftbar = canvas.getContext('2d')
  drawBottomLeftBar(bottomleftbar, numberArray[4])

  const bottomrightbar = canvas.getContext('2d')
  drawBottomRightBar(bottomrightbar, numberArray[5])

  const bottombar = canvas.getContext('2d')
  drawBottomBar(bottombar, numberArray[6])
}

const drawTopBar = (ctx, num) => {
  ctx.beginPath()
  ctx.moveTo(25, 12)
  ctx.lineTo(29, 7)
  ctx.lineTo(74, 7)
  ctx.lineTo(78, 12)
  ctx.lineTo(69, 18)
  ctx.lineTo(30, 18)
  ctx.lineTo(25, 12)
  ctx.stroke()
  if (num == 1) {
    ctx.fillStyle = OnColor
  } else {
    ctx.fillStyle = OffColor
  }
  ctx.fill()
}

const drawTopLeftBar = (ctx, num) => {
  //top left bar
  ctx.beginPath()
  ctx.moveTo(24, 13)
  ctx.lineTo(19, 19)
  ctx.lineTo(14, 58)
  ctx.lineTo(18, 62)
  ctx.lineTo(25, 56)
  ctx.lineTo(29, 19)
  ctx.lineTo(24, 13)
  ctx.stroke()
  if (num == 1) {
    ctx.fillStyle = OnColor
  } else {
    ctx.fillStyle = OffColor
  }
  ctx.fill()
}

const drawTopRightBar = (ctx, num) => {
  //top right bar
  ctx.beginPath()
  ctx.moveTo(77, 13)
  ctx.lineTo(73, 19)
  ctx.lineTo(68, 58)
  ctx.lineTo(72, 62)
  ctx.lineTo(79, 56)
  ctx.lineTo(83, 19)
  ctx.lineTo(77, 13)
  ctx.stroke()
  if (num == 1) {
    ctx.fillStyle = OnColor
  } else {
    ctx.fillStyle = OffColor
  }
  ctx.fill()
}

const drawMiddleBar = (ctx, num) => {
  //middle bar
  ctx.beginPath()
  ctx.moveTo(18, 63)
  ctx.lineTo(22, 58)
  ctx.lineTo(67, 58)
  ctx.lineTo(71, 63)
  ctx.lineTo(62, 69)
  ctx.lineTo(23, 69)
  ctx.lineTo(18, 63)
  ctx.stroke()
  if (num == 1) {
    ctx.fillStyle = OnColor
  } else {
    ctx.fillStyle = OffColor
  }
  ctx.fill()
}

const drawBottomLeftBar = (ctx, num) => {
  //bottom left bar
  ctx.beginPath()
  ctx.moveTo(17, 65)
  ctx.lineTo(12, 71)
  ctx.lineTo(7, 110)
  ctx.lineTo(11, 114)
  ctx.lineTo(18, 108)
  ctx.lineTo(22, 71)
  ctx.lineTo(17, 65)
  ctx.stroke()
  if (num == 1) {
    ctx.fillStyle = OnColor
  } else {
    ctx.fillStyle = OffColor
  }
  ctx.fill()
}

const drawBottomRightBar = (ctx, num) => {
  //bottom right bar
  ctx.beginPath()
  ctx.moveTo(70, 64)
  ctx.lineTo(66, 70)
  ctx.lineTo(61, 109)
  ctx.lineTo(65, 113)
  ctx.lineTo(72, 107)
  ctx.lineTo(76, 70)
  ctx.lineTo(70, 64)
  ctx.stroke()
  if (num == 1) {
    ctx.fillStyle = OnColor
  } else {
    ctx.fillStyle = OffColor
  }
  ctx.fill()
}

const drawBottomBar = (ctx, num) => {
  //bottom bar
  ctx.beginPath()
  ctx.moveTo(11, 113)
  ctx.lineTo(15, 108)
  ctx.lineTo(60, 108)
  ctx.lineTo(64, 113)
  ctx.lineTo(55, 119)
  ctx.lineTo(16, 119)
  ctx.lineTo(11, 113)
  ctx.stroke()
  if (num == 1) {
    ctx.fillStyle = OnColor
  } else {
    ctx.fillStyle = OffColor
  }
  ctx.fill()
}
</script>

<style lang="css" scoped>
.counter-container {
  width: 300px;
  display: flex;
  justify-content: center;
  position: fixed;
  right: -70px;
  bottom: -30px;
  background-color: transparent;
  scale: 0.5;
}

.speedometer {
  background-color: grey;
}

canvas {
  background-color: black;
  border: 2px solid white;
}

.space {
  padding: 3%;
}

.buttonbox {
  background-color: grey;
}
</style>
