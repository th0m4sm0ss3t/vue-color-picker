<template>
  <div class="grid">
    <div 
      class="grid-item"
      v-for="(block, id) in blocks"
      :key="id"
      :style="'background:'+block.color"
      @click="setBlockColor(id)"
    >

      </div>
  </div>
</template>

<script>
export default {
    name: "ColorGrid",
    props: ['color'],
    data () {
        return {
            blocks: [],
            gridSize: 100,
        }
    },
    methods: {
        initGrid () {
            for (let i = 0; i < this.gridSize; i++) {
                this.blocks.push({
                    color: "#FFF",
                });
            }
        },
        setBlockColor (id) {
            this.blocks[id].color = this.color;
        }
    },
    created () {
        this.initGrid();
    },
}
</script>

<style scoped>
.grid {
    display: grid;
    grid-template-columns: repeat(10, 1fr);
    grid-template-rows: repeat(10, 1fr);
    width: 320px;
    height: 320px;
    margin: 5rem auto;
}
.grid-item {
    border: 1px dashed #CCC;
}
</style>