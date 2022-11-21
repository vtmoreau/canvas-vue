<template>
  <div id="app">
    <CanvasHome/>
  </div>
</template>

<script>
import CanvasHome from './components/CanvasHome.vue'
export default {
  name: 'App',
  components: {
    CanvasHome
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
