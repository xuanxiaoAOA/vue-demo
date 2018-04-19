<template>
  <div id="app">
    <!-- 将路由组件化 -->
    <header-col/>
    <router-view/>
  </div>
</template>

<script>
import Header from './components/Header'
export default {
  name: 'App',
  components: {
    'header-col': Header
  }
}
</script>

<style>
*{
  margin:0;
  padding:0;
}
body,html{
  width: 100%;
  height: 100%;
}
a{
  text-decoration: none;
  outline: none;
  color:#000;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100%;
}
</style>
