<template>
  <div class="color-picker">
    <div 
      class="color"
      v-for="(color, i) in colors"
      :key="i"
      :style="'background:'+color"
      @click="setColor(color)"></div>
  </div>
</template>

<script>
export default {
  name: 'color-picker',
  props: ['colors'],
  methods: {
    setColor (color) {
      this.$emit('setColor', color);
    }
  }
}
</script>

<style scoped>
.color-picker {
  width: 125px;
  display: grid;
  margin: 15px auto;
  grid-template-columns: repeat(5, 25px);
}
.color {
  border: 1px solid #AAA;
  height: 25px;
}
</style>

