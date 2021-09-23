<template>
  <div>
    <Header :color="color"/>
    <ColorPicker :colors="colors" @setColor="setColor" />
    <ColorGrid :color="color" />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import ColorPicker from './components/ColorPicker.vue'
import ColorGrid from './components/ColorGrid.vue'

export default {
  name: 'App',
  components: {
    Header,
    ColorPicker,
    ColorGrid,
  },
  data() {
    return {
      colors: ["#FFF", "#000", "#AF1E2D", "#00EEAE", "#FFCE00"],
      color: "#FFF",
    }
  },
  methods: {
    setColor (color) {
      this.color = color;
    },
  },
}
</script>

<style>
body {
  margin: 0;
  padding: 0;
  background: #f3f3f3;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
