<template>
<div>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <HelloWorld msg="Welcome to Your Vue.js App"/>
<homefile/>
</div>
</template>

<script>
// import HelloWorld from './components/Hello-World.vue'
import homefile from './components/homefile.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld,
    homefile
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
