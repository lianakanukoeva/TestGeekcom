<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <HelloWorld />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style lang="scss">
body {
  font-size: 16px;
  margin: 0;
  padding: 0;
  line-height: 1.42;
  position: relative;
}

*, *::before, after{
  box-sizing: border-box;
}

body, html {
  widows: 100%;
  height: 100%;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  background-color: #EFF3F5;
}
</style>
