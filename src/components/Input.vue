<template>
  <div class="input-box">
		<input type="text" v-model="task">
		<button type="submit"> ADD TASK </button>
	</div>	
</template>

<script>
export default {
  name: 'Input',
	data() {
		return {
			task: 'Try creating this new task'
	}}
}
</script>

<style scoped>

div {
	display: flex;
	margin-bottom: 50px;
	height: 5em;
	width: 70%;
	border-radius: 10px;
	box-shadow: 3px 3px 10px #0000003f;
}

input {
	font-size: 2em;
	height: 100%;
	width: 75%;
	border: none;	
	border-radius: 10px 0px 0px 10px;
	text-indent: 0.5em;
	color: #16161627;
}

input:focus {
	color: #333433;
	outline: none;
}

button {
	height: 100%;
	width: 25%;
	border: none;
	color: #fff;
	background-color: #333433;	
	border-radius: 0px 10px 10px 0px;
}
.input-box button:hover {
	background-color: #262726;	
}
</style>
