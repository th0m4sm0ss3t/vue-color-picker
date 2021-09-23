<template>
  <header class="header">
    <h1>Color <span>Picker</span></h1>
    <div 
      class="color"
      :style="'background:'+color"
    >
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
  props: ['color'],
}
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-content: center;
  height: 60px;
  background: #171717;
  padding: 0 1rem;
  align-items: center;
}

h1 {
  color: #f3f3f3;
  font-size: 1.75rem;
  font-weight: 300;
  text-transform: uppercase;
}

h1 span {
  color: #ffce00;
  font-weight: 900;
}

.color {
  border: 1px dashed #f3f3f3;
  width: 25px;
  height: 25px;
}

</style>
