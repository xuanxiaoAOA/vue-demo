<template>
	<div>
		<TodoList/>
		<my-component></my-component>
		<div id="app2">
			<span>{{msg}}</span>
			<simple-counter></simple-counter>
			<simple-counter></simple-counter>
			<simple-counter></simple-counter>
		</div>
		<div id="app">
			<input v-model="parentMsg">
			<br>
			<child v-bind:my-message="parentMsg"></child>
		</div>
	</div>
</template>

<script>
import Header from '../../components/Header'
import TodoList from '../../components/TodoList'
import simple_counter from '../../components/simple-counter'
var childrr = {
	template:'<div>局部组件的使用</div>'
}
export default {
	name:'Plus',
	components: {
		TodoList,
		'my-component':childrr,
		'simple-counter':simple_counter,
		child: {  
            props: ['myMessage'],  
            template: '<span>{{myMessage}}</span>'  
    	}  
	},
	data (){
		return {
			msg:'全局组件',
			parentMsg: 'Message from parent'  
		}
	}

}

</script>