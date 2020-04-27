<template>
  <div id="app">
    <FlipList/>
  </div>
</template>

<script>
import FlipList from './components/FlipList.vue'

export default {
  name: 'App',
  components: {
    FlipList
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
