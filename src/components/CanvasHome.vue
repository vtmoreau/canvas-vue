<template>
  <div>
        
    <h1>Simple Canvas App</h1>

    <h2>x: {{ x_ }}, y: {{ y_ }}</h2>

    <div class="row">
    <vue-drawing-canvas
      ref="VueCanvasDrawing"
      width="600"
      height="400"
      @mousemove="getCoordinates($event)"
      :styles="{
        border: 'solid 1px black',
      }"
    />
    </div>
    

    <button @click="showStrokes">Strokes</button>

  </div>
</template>

<script>
  import VueDrawingCanvas from "vue-drawing-canvas";

  export default {
    components: {
      VueDrawingCanvas,
    },
    data() {
      return {
        x_: null,
        y_: null  
      }
    },
    methods: {
      getCoordinates() {
        let coords = this.$refs.VueCanvasDrawing.getCoordinates(event);
        this.x_ = coords.x;
        this.y_ = coords.y;
      },
      showStrokes() {
        console.log(this.$refs.VueCanvasDrawing.getAllStrokes())
      }
    }
  }
</script>

<style scoped>
.row {
  display: flex;
  justify-content: center;
}
</style>
