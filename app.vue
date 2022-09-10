<template>
  <div id="app">
    <grid-lines />
    <scrambler />

    <footer>
      <a href="mailto:team@kanban.ee?subject=Hi%20there%20👋" class="contact-link">team@kanban</a>
    </footer>
  </div>
</template>

<style>
:root {
  --highlight: rgb(142, 197, 252);
  --content: #fefefe;
  --background: #222;
  --padding: 2rem;
  --font: 'SFMono-Regular', Menlo, Consolas, 'Liberation Mono', Courier, monospace;
}

/* Handcraft reset */
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
  padding: var(--padding);
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
  color: inherit;
}

::placeholder {
  color: var(--highlight);
}
::selection {
  background-color: var(--highlight);
  color: white;
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
  background-color: var(--background);
  box-shadow: 0px 2px 6px rgba(45, 55, 72, 0.1), 0px 2px 4px rgba(45, 55, 72, 0.06);
  /* TODO: Add light randomized animation? */
  clip-path: polygon(0 0, 82% 0, 100% 20%, 100% 100%, 15% 100%, 0 80%);
}

footer {
  position: absolute;
  bottom: 35vh;
  color: white;
  font-family: var(--font);
  text-align: center;
  font-size: 1rem;
}
.contact-link {
  position: relative;
  display: inline-block;
  padding: 1.5rem;
  transition: transform cubic-bezier(0.075, 0.82, 0.165, 1) 0.2s;
  transform: scale(1);
  cursor: pointer;
  z-index: 3;
  letter-spacing: 2.6px;
  text-decoration: none;
}
.contact-link:hover {
  transform: scale(1.0825);
}

@media screen and (max-width: 40rem) {
  html {
    font-size: 0.8rem;
  }
}
</style>
