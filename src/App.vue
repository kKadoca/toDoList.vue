<template>
	<Header></Header>
	<div class="content">
		<Input></Input>
		<Task></Task>
	</div>
</template>

<script>
import Header from './components/Header.vue'
import Input from './components/Input.vue'
import Task from './components/Task.vue'

export default {
  name: 'App',
  components: {
    Header,
		Input,
		Task
  }
}
</script>

<style>
* {
	margin: 0;
	padding: 0;
}

body {
	height: 100vh;
	width: 100%;
	display: flex;
	flex-direction: column;
	background-color: #f6f6f6;
}

#app {
	margin: 0;
	padding: 0;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
}

.content {
	display: flex;
	flex-direction: column;
	align-items: center;
}
</style>
