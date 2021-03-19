<template>
<div>
  <div id="nav">
    <router-link to="/">READ</router-link>
    <router-link to="/home" class="home" >WRITE</router-link>
  </div>
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
body{
  margin: 0;
  padding: 0;
  background-color: rgba(255, 255, 255, 0.938);
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
#nav {
  text-align: center;
  background-color: rgb(250, 237, 237);
  line-height: 60px;
  width: 100%;
  position: fixed;
  top: 0;
}
#nav a {
  font-size: 20px;
  text-decoration: none;
  margin: 0 30px;
}
#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
