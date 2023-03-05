<template>
  <div>
		<p>Titulo</p>
		<button class="red">Excluir</button>
		<button class="green">Concluida</button>
	</div>	
</template>

<script>
export default {
  name: 'Task'
}
</script>

<style scoped>

div {
	display: flex;
	margin-bottom: 20px;
	height: 5em;
	width: 70%;
	border-radius: 10px;
	box-shadow: 3px 3px 10px #0000003f;
}

p {
	font-size: 2em;
	height: 100%;
	width: 70%;
	background-color: #fff;
	border-radius: 10px 0px 0px 10px;
}

button {
	height: 100%;
	width: 15%;
	border: none;
}

.red {
	background-color: rgb(251, 129, 129);
}

.green {
	background-color: rgb(138, 244, 138);
	border-radius: 0px 10px 10px 0px;
}

</style>