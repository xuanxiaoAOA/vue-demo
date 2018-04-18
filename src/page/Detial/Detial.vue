<template>
  <div @click='show'>
    详情 点击看参数
  </div>
</template>
<script>
export default {
	name: 'Detail',
	methods: {
		show(){
			console.log(this.$router.parmars)
		}
	}
}
</script>
<style >
</style>
