<template>
  <div class="amount">
    <div style="display: flex">
      <span>￥</span>
      <transition-group name="list" tag="p" style="position: relative">
        <div
          style="display: inline-block; position: absolute"
          v-for="(item, index) in todayAmountComputed"
          :style="{
            left: index * 53 + 'px',
            'transition-delay': 0.1 * index + 's'
          }"
          :key="item + index"
        >
          {{ item }}
        </div>
      </transition-group>
    </div>
  </div>
</template>
<script setup lang="ts">
import { reactive, computed, onMounted } from 'vue'
const data = reactive({
  todayAmount: '0',
  platformSales1: 4090013
})

const todayAmountComputed = computed(() => {
  return data.todayAmount.split('')
})

onMounted(() => {
  //   setInterval(() => {
  //     if (data.todayAmount === '0') {
  //       data.todayAmount = '1000'
  //     }
  //     data.todayAmount = '' + Math.floor(Math.random() * 10000)
  //   }, 2000)
})
</script>
<style>
* {
  margin: 0px;
  padding: 0px;
}

body,
html {
  width: 100%;
  height: 100%;
}

#app {
  position: relative;
}

.amount {
  color: gold;
  font-size: 85px;
  display: flex;
  justify-content: center;
}

.list-enter-active,
.list-leave-active {
  transition: transform 1s ease, opacity 1s ease;
}

.list-enter-from {
  opacity: 0;
  transform: translateY(50%);
}

.list-leave-to {
  opacity: 0;
  transform: translateY(-50%);
}
</style>
