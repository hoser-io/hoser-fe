<template>
  <div style="margin: 2rem">
    <div class="hero">
      <img alt="Hoser logo" src="./assets/logo.png">
      <h1>Hoser</h1>
    </div>
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
  color: #90330;
  margin-top: 60px;
}

.hero {
  text-align: center;
}
body {
  background-color: #494847;
  color: white;
}
</style>
