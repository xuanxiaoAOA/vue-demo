<template>

		<button v-on:click="counter += 1">{{counter}}</button>
		
</template>
<script type="text/javascript">
	export default{
		data(){
			return {
				counter:0
			}
		}
	}
</script>