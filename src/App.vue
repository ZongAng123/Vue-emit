<template>
  <div id="app">
    <FuQin />
  </div>
</template>

<script>
import FuQin from './components/FuShiTu.vue' //父视图

export default {
  name: 'App',
  components: {
    FuQin
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
  margin-top: 00px;
}
</style>
