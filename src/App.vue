<template>
  <div id="app">
    <to-do></to-do>
    <router-view/>
  </div>
</template>

<script>
import ToDo from './components/ToDo'
export default {
  name: 'App',
  components: {
    ToDo
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
