<script setup>
// defineProps({
//   msg: {
//     type: String,
//     required: true
//   }
// })

import { reactive } from 'vue'

let nowTime = reactive({
  data: ""
})
let nowDate = reactive({
  data: ""
})

let currentDate = new Date()

function setTime(date) {
  const day = date.toDateString() // Sat Dec 24 2022
  const time = date.toTimeString().slice(0, 8) // 23:57:45 GMT+0800 (台北標準時間)
  nowDate.data = day
  nowTime.data = time
}

function getNowTime() {
  setTime(currentDate)
  setInterval(() => {
    currentDate = new Date()
    setTime(currentDate)
  }, 1000)
}
getNowTime()

</script>

<template>
<div class="container-fluid">
  <h1>Hello</h1>
  <h1>{{ nowTime.data }}</h1>
  <h5>{{ nowDate.data }}</h5>
</div>
</template>

<style scoped>
</style>
