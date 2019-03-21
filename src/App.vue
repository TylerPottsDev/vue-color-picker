<template>
  <div id="app">
    <Header :color="color" />
    <ColorPicker :colors="colors" @setColor="setColor" />
    <ColorGrid :color="color" />
  </div>
</template>

<script>
import Header from '@/components/Header';
import ColorPicker from '@/components/ColorPicker';
import ColorGrid from '@/components/ColorGrid';

export default {
  name: 'app',
  components: {
    Header,
    ColorPicker,
    ColorGrid
  },
  data () {
    return {
      colors: ["#FFF", "#000", "#AF1E2D", "#00EEAE", "#FFCE00"],
      color: "#FFFFFF"
    }
  },
  methods: {
    setColor (color) {
      this.color = color;
    }
  }
}
</script>

<style>
body {
  margin: 0;
  padding: 0;
  background: #F3F3F3;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
