<template>
  <div :class="$style.container">
    <div :class="$style.text" ref="container"></div>
  </div>
</template>

<script>
import TextScramble from '../scrambler'

const phrases = ['Kanban', 'consultation', 'kanban;', 'technical review', '.kanban()', 'development']

export default {
  name: 'Scrambler',
  async mounted () {
    await this.$nextTick()
    const fx = new TextScramble(this.$refs.container)

    let counter = 0
    const next = () => {
      fx.setText(phrases[counter]).then(() => {
        setTimeout(next, 800)
      })
      counter = (counter + 1) % phrases.length
    }

    next()
  }
}
</script>

<style module>
.container {
  height: 100%;
  width: 100%;
  justify-content: center;
  align-items: center;
  display: flex;
}
.text {
  font-weight: 100;
  font-size: 28px;
  color: #fafafa;
}
:global(.dud) {
  color: #757575;
}
</style>
