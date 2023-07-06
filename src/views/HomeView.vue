<script setup lang="ts">
import { ref } from 'vue'
import Num from '../components/NumAnimate.vue'
import NumCount from '../components/NumCountTo.vue'
const ns = ref([0, 0, 0, 0, 0])
setInterval(() => {
  ns.value.forEach((v, i) => {
    ns.value[i] = Math.ceil(Math.random() * 100) % 10
  })
  console.log(ns.value)
}, 3000)
</script>

<template>
  <div class="wrap">
    <div class="flex">
      <Num :number="ns"></Num>
    </div>
    <NumCount :number="ns"></NumCount>
  </div>
</template>
<style lang="scss" scoped>
.flex {
  display: flex;
}
.wrap {
  height: 100vh;
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
  grid-template-rows: repeat(auto-fill, minmax(280px, 1fr));
}
</style>
