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
  font-family: inherit;
  font-size: 3rem;
  color: white;

  .typed-cursor {
    font-size: 1.875rem;
    background-color: white;
  }
}
</style>
