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
.btn{
  position: relative;
  display: inline-block;
  padding: 6px 12px;
  font-size: 14px;
  font-weight: 600;
  line-height: 20px;
  white-space: nowrap;
  vertical-align: middle;
  cursor: pointer;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  background-repeat: repeat-x;
  background-position: -1px -1px;
  background-size: 110% 110%;
  border: 1px solid rgba(27, 31, 35, 0.2);
  border-radius: 0.25em;
  -webkit-appearance: none;
  -moz-appearance: none;
  appearance: none
}
.btn:hover{
  background-color: #e6ebf1;
  background-image: linear-gradient(-180deg, #f0f3f6 0%, #e6ebf1 90%);
  background-position: -.5em;
  border-color: rgba(27, 31, 35, 0.35)
}
.btn-primary{
  color: #fff;
  background-color: #28a745;
  background-image: linear-gradient(-180deg, #34d058 0%, #28a745 90%)
}
.btn-primary:hover{
  background-color: #269f42;
  background-image: linear-gradient(-180deg, #2fcb53 0%, #269f42 90%);
  background-position: -.5em;
  border-color: rgba(27, 31, 35, 0.5)
}
.shelf-cta{
  padding: 10px 50px;
  font-size: 16px
}
</style>
