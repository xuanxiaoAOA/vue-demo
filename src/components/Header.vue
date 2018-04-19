<template>
  <div class="header">
    <router-link active-class='active_header' to="/home">首页</router-link>
    <router-link active-class='active_header' to="/product">产品</router-link>
    <router-link active-class='active_header' to="/plus">plus</router-link>
    <router-link active-class='active_header' :to="{path:'/detial',query: {id:1}}">详情带参数</router-link>
    <el-button type="success" @click='goBack'>js返回前一页</el-button>
  </div>
</template>
<script>
export default {
  name: 'Header',
  methods: {
		goBack(){
      this.$router.go(-1)
			console.log(this.$router.params);
		}
	}
}
</script>
<style >
.header{
	background: #999;
}
.active_header{
  color: #fff;
}
</style>
