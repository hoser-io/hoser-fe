<template>
  <div>
    <img alt="Hoser logo" src="./assets/logo.png">
    <h1>Hoser</h1>
    <HoserMain/>
  </div>
</template>

<script>
import HoserMain from './components/HoserMain.vue'

export default {
  name: 'App',
  components: {
    HoserMain
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
