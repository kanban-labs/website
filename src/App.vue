<template>
  <div id="app">
    <grid-lines />

    <typer />

    <footer>
      <p>consultation · review · development</p>
      <p>📧 <a href="mailto:team@kanban.ee?subject=Hi%20there%20👋" class="contact-link">team@kanban</a></p>
    </footer>
  </div>
</template>

<script>
import Typer from './components/Typer'
import GridLines from './components/GridLines'

export default {
  name: 'app',
  components: { Typer, GridLines }
}
</script>

<style lang="scss">
:root {
  --highlight: rgb(142, 197, 252);
  --content: #fefefe;
  --background: #222;
  --padding: 2rem;
  --font: 'SFMono-Regular', Menlo, Consolas, 'Liberation Mono', Courier, monospace;
  --font-alt: -apple-system, system-ui, BlinkMacSystemFont, 'Segoe UI', Roboto, Ubuntu;
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
  padding: var(--padding);
}
@media screen and (max-width: 40rem) {
  :root {
    --padding: 1rem;
  }
}
#app {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  position: relative;
  height: calc(100vh - 2 * var(--padding));
  width: 100%;
  border-radius: 0.5rem;
  background-color: var(--background);
  box-shadow: 0px 2px 6px rgba(45, 55, 72, 0.1), 0px 2px 4px rgba(45, 55, 72, 0.06);
}
body,
button,
input,
textarea {
  font-family: var(--font);
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

footer {
  position: absolute;
  bottom: 32vh;
  color: white;
  font-family: var(--font);
  text-align: center;
  font-size: 1rem;
}
footer p:last-child {
  margin-top: 1rem;
}
.contact-link {
  letter-spacing: 2.6px;
}
</style>
