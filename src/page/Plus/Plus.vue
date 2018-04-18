<template>
	<div>
		<h1>My Todo App!</h1>
		<TodoList/>
		<router-view/>
	</div>
</template>

<script>
import TodoList from '../../components/TodoList'

export default {
	name:'Plus',
	components: {
		TodoList
	}
}
</script>