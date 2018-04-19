<template>
	<div id="example">
		<el-button type="primary" v-on:click="greet">Greet</el-button>
	</div>
</template>
<script type="text/javascript">
	export default {
		name: 'TodoList',
		data(){
			return{
				name: 'Vue.js'
			}
			
		},
		methods : {
			greet: function (event){
				alert('hello' + this.name + '~')
				if(event){
					alert(event.target.tagName)
				}
			}
		}
	}
</script>