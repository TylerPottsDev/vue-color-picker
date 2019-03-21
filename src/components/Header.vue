<template>
  <header>
    <h3>Color<span>Picker</span></h3>
    <div class="color" :style="'background:'+color"></div>
  </header>
</template>

<script>
export default {
  name: 'header-nav',
  props: ['color']
}
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 60px;
  background: #171717;
  padding: 0px 15px;
}
h3 {
  color: #F3F3F3;
  font-size: 28px;
  font-weight: 300;
  text-transform: uppercase;
}
h3 span {
  color: #FFCE00;
  font-weight: 900;
}
.color {
  width: 25px;
  height: 25px;
  border: 1px dashed #F3F3F3;
}
</style>


