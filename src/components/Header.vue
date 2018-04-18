<template>
  <div class="header">
    <router-link to="/home">首页</router-link>
    <router-link to="/product">产品</router-link>
    <router-link to="/">返回/ 组件化的</router-link>
  </div>
</template>
<script>
export default {
  name: 'Header'
}
</script>
<style >
.header{
	background: #000;
}
.header a{
	color: #fff
}
</style>
