<template>
  <div class="color-picker">
    <div 
        class="color"
        v-for="(color, id) in colors"
        :key="id"
        :style="'background:'+color"
        @click="setColor(color)"
    >

    </div>
  </div>
</template>

<script>
export default {
  name: "ColorPicker",
  props: ['colors'],
  methods: {
    setColor (color) {
        this.$emit('setColor', color);
    },
  },
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
    height: 25px;
    cursor: pointer;
}
</style>