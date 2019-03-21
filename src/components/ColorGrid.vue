<template>
  <div class="grid">
    <div
      class="grid-item"
      v-for="(block, i) in blocks"
      :key="i"
      :style="'background:'+block.color"
      @click="setBlockColor(i)"></div>
  </div>
</template>

<script>
export default {
  name: 'color-grid',
  props: ['color'],
  data () {
    return {
      blocks: [],
      gridSize: 100
    }
  },
  methods: {
    initGrid () {
      for (let i = 0; i < this.gridSize; i++) {
        this.blocks.push({
          color: "#FFF"
        });
      } 
    },
    setBlockColor (i) {
      this.blocks[i].color = this.color;
    } 
  },
  created () {
    this.initGrid();
  }
}
</script>

<style scoped>
.grid {
  display: grid;
  grid-template-columns: repeat(10, 1fr);
  grid-template-rows: repeat(10, 1fr);
  width: 320px;
  height: 320px;
  margin: 0 auto;
}
.grid-item {
  border: 1px dashed #CCC;
}
</style>
