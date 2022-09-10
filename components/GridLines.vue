<template>
  <div class="lines">
    <div v-for="i in 8" :key="i" class="line" :style="{ left: `${(i - 1) * Math.round(100 / 8) + 10}%` }"></div>
  </div>
</template>

<style>
.line {
  position: fixed;
  width: 1px;
  height: calc(100vh - 2 * var(--padding));
  top: var(--padding);
  background-color: #313131;
}
</style>
