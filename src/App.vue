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
  background-image: linear-gradient(62deg, rgb(142, 197, 252) 0%, rgb(224, 195, 252) 100%);
  // background-image: linear-gradient(66deg, rgb(254, 225, 64) 0%, rgb(250, 112, 154) 100%);
  padding: 2rem;
}
#app {
  height: calc(100vh - 4rem);
  width: 100%;
  background-color: var(--background);
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 0.5rem;
  box-shadow: 0px 2px 6px rgba(45, 55, 72, 0.1), 0px 2px 4px rgba(45, 55, 72, 0.06);
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
  // text-decoration-width: 2px;
}

::placeholder {
  color: var(--highlight);
}
::selection {
  background-color: var(--highlight);
  color: white;
}
</style>
