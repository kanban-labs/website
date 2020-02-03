<template>
  <div class="wrapper">
    <vue-typed-js
      :strings="['Kanban', 'Kan{b}an', 'kanban;', 'Kan}an']"
      :smartBackspace="false"
      :loop="true"
      :shuffle="false"
      :startDelay="70"
      :typeSpeed="70"
      :backDelay="1600"
      :backSpeed="70"
      erase-style="backspace"
      :erase-on-complete="false"
      caret-animation="smooth"
      ><h1 class="typing"></h1
    ></vue-typed-js>
  </div>
</template>

<script>
import { VueTypedJs } from 'vue-typed-js'

export default {
  name: 'typer',
  components: { VueTypedJs }
}
</script>

<style lang="scss">
.wrapper {
  position: relative;
  z-index: 1;
  font-family: var(--font);
  font-size: 2rem;
  color: white;

  .typed-cursor {
    font-size: 2.75rem;
    background-color: white;
  }
}
</style>
