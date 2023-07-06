<template>
  <div class="amount">
    <!-- <span>￥</span> -->
    <transition-group name="list" tag="div" style="position: relative">
      <div
        style="display: inline-block; position: absolute"
        v-for="(item, index) in number"
        :style="{
          left: index * 53 + 'px',
          'transition-delay': 0.1 * index + 's'
        }"
        :key="item + '-' + index"
      >
        {{ item }}
      </div>
    </transition-group>
  </div>
</template>
<script setup lang="ts">
withDefaults(defineProps<{ number: number[] }>(), {
  number: () => []
})
</script>
<style>
.amount {
  color: gold;
  font-size: 85px;
  display: flex;
  justify-content: center;
  align-items: center;
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
