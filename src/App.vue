<template>
  <div id="app">
    <LandingPage msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import LandingPage from './components/LandingPage.vue'

export default {
  name: 'App',
  components: {
    LandingPage
  }
}
</script>

<style>
html{
  height: 100%;
}
body, #app{
  height: 100%;
  width: 100%;
}
#app {
  font-family: 'Figtree', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2D4E63;
}
</style>
