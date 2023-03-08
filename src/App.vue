<template>
	<Header></Header>
	<div class="content">
		<ToDoList></ToDoList>
	</div>
	<Footer></Footer>
</template>

<script>
import Header from './components/Header.vue'
import ToDoList from './components/ToDoList.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
		ToDoList,
		Footer
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
	min-width: 400px;
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
