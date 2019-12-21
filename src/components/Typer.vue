<template>
  <div class="wrapper">
    <vue-typer
      :text="['Kanban', 'Kan{b}an', 'kanban;', 'Kan}an']"
      :repeat="Infinity"
      :shuffle="false"
      initial-action="typing"
      :pre-type-delay="70"
      :type-delay="70"
      :pre-erase-delay="1600"
      :erase-delay="60"
      erase-style="backspace"
      :erase-on-complete="false"
      caret-animation="smooth"
    />
  </div>
</template>

<script>
import { VueTyper } from 'vue-typer'

export default {
  name: 'typer',
  components: { VueTyper }
}
</script>

<style lang="scss">
.wrapper {
  .vue-typer {
    font-family: inherit;
    font-size: 3rem;
  }
  .vue-typer .custom.char.typed {
    color: white;
  }
  .vue-typer .custom.caret {
    width: 6px;
    background-color: white;
  }
}
</style>
