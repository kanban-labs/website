<template>
  <div class="lines">
    <div v-for="i in 6" :key="i" class="line" :style="{ left: `${--i * 20 + 10}%` }"></div>
  </div>
</template>

<style>
.lines {
  display: flex;
  align-items: center;
  justify-content: center;
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  bottom: var(--padding);
  left: 0;
  pointer-events: none;
}
.line {
  position: absolute;
  width: 1px;
  height: calc(100vh - 2 * var(--padding));
  top: 0;
  background: #313131 none repeat scroll 0% 0%;
  opacity: 1;
  transform-origin: 50% 0% 0px;
}
</style>
