<template>
  <div id="app">
    <typer />
  </div>
</template>

<script>
import Typer from './components/Typer'

export default {
  name: 'app',
  components: { Typer }
}
</script>

<style lang="scss">
:root {
  --highlight: tomato;
  --content: #fefefe;
  --background: #222;
}

/* Handicraft reset */
*,
*::before,
*::after {
  box-sizing: inherit;
}
html {
  box-sizing: border-box;
}
body,
body * {
  margin: 0;
  padding: 0;
}
body {
  min-height: 100vh;
  height: 100%;
  background-color: var(--highlight);
  padding: 1rem;
}
#app {
  height: calc(100vh - 2rem);
  width: 100%;
  background-color: var(--background);
  display: flex;
  align-items: center;
  justify-content: center;
}
body,
button,
input,
textarea {
  font-family: -apple-system, system-ui, BlinkMacSystemFont, 'Segoe UI', Roboto, Ubuntu;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

ol,
ul {
  list-style: none;
}

/* Global styles */
h1 {
  font-size: 1.875rem;
  line-height: 2.25rem;
  color: var(--content);
  font-weight: 700;
}

button {
  display: block;
  border: none;
  background: none;
  color: inherit;
  font-size: inherit;
}
button[disabled],
.cursor-disabled {
  cursor: not-allowed;
}
label,
button,
.cursor-pointer {
  cursor: pointer;
}
.break-all {
  word-break: break-all;
}
.break-word {
  word-break: break-word;
}

a {
  text-decoration-style: dashed;
  color: inherit;
}
a:hover {
  text-decoration-style: solid;
  text-decoration-width: 2px;
}

::placeholder {
  color: var(--highlight);
}
::selection {
  background-color: var(--highlight);
  color: white;
}
</style>
