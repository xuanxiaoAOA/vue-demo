<template>
  <div class="content">
    产品
  </div>
  
</template>
<script>
export default {
	name: 'Product',
	methods: {
		goBack(){
			console.log(this.$router.go(-1));
		}
	}
}
</script>
<style >
  .content{
  }
</style>
