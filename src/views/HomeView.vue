<script setup lang="ts">
import { ref } from 'vue'
import Num from '../components/NumAnimate.vue'
import NumCount from '../components/NumCountTo.vue'
const ns = ref([0, 0, 0, 0, 0])
// setInterval(() => {
//   ns.value.forEach((v, i) => {
//     ns.value[i] = Math.ceil(Math.random() * 100) % 10
//   })
//   console.log(ns.value)
// }, 3000)
</script>

<template>
  <main>
    <div class="flex">
      <Num v-for="(n, i) in ns" :key="i" :number="n"></Num>
    </div>
    <NumCount></NumCount>
  </main>
</template>
<style>
.flex {
  display: flex;
}
</style>
