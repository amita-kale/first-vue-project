<template>
<div>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/>
<homefile demo="Welcome to my first webpage"/> -->
<Home/>
</div>
</template>

<script>
// import HelloWorld from './components/Hello-World.vue'
//import homefile from './components/homefile.vue'
import Home from './components/Home.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld,
    //homefile,
    Home,
    
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
  /* margin-top: 60px; */
}
</style>
