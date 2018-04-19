<template>
  <div class="header">
    <router-link active-class='active_header' to="/home">首页</router-link>
    <router-link active-class='active_header' to="/product">产品</router-link>
    <router-link active-class='active_header' to="/plus">plus</router-link>
    <router-link active-class='active_header' :to="{path:'/detial',query: {id:1}}">详情带参数</router-link>
    <div class="btn btn-primary" @click='goBack'>js返回前一页</div>
    <div id="example-5">
      <select v-model="selected">
        <option disabled value="">请选择</option>
        <option>A</option>
        <option>B</option>
        <option>C</option>
      </select>
      <span>Selected: {{ selected }}</span>
    </div>
  </div>
</template>
<script>
export default {
  name: 'Header',
  data(){
    return {
      selected:''
    }
  },
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
