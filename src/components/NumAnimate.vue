<template>
  <div class="box" v-for="(n, i) in number" :key="i">
    <span class="num" :style="`transform: translate(-50%, -${n * 10}%)`">0123456789</span>
  </div>
</template>

<script setup lang="ts">
withDefaults(defineProps<{ number: number[] }>(), {
  number: () => []
})
</script>

<style lang="scss" scoped>
.box {
  height: 82px;
  width: 54px;
  line-height: 82px;
  text-align: center;
  background-color: #149373;
  border-radius: 10px;
  overflow: hidden;
  margin-right: 5px;

  position: relative;
  writing-mode: vertical-lr;
  text-orientation: upright;
  &:last-of-type {
    margin-right: 0;
  }
}
.num {
  position: absolute;
  left: 50%;
  top: 0px;
  font-size: 62px;
  color: #ffffff;
  transition: all 1.5s;
}
</style>
