<template>
  <div id="app">
    <Header/>
    <router-view/>
  </div>
</template>

<script>

import Header from './components/layout/Header';
export default {
  name:"app",
  components:{
    Header
  }
}
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left; 
  color: #2c3e50;
}

#nav {
  padding: 1px;
}

#nav a {
  font-weight: bold;
  color: #ffffff;
}

#nav a.router-link-exact-active {
  color: #ffffff;
}
</style>
