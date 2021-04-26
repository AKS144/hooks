<template>
  <div id="app">
    <h1>Make Form</h1> 
    <login2 />
  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
//import login from './components/login.vue'
import login2 from './components/login2.vue'

export default {
  name: 'App',
  components: {
    //HelloWorld
    //login
    login2
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
