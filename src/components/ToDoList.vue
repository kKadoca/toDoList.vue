<template>
    <div>
        <form @submit.prevent="addTask">
            <input type="text" v-model="newTask">
            <button type="submit"> ADD TASK </button>
        </form>
        <ul>
			<li v-for="(task, index) in tasks" :key="index">
				<p> {{ task }}</p>
				<button class="red">Excluir</button>
				<button class="green">Concluida</button>
			</li>
		</ul>
    </div>	
</template>
  
<script>
    export default {
        data() {
            return {
                tasks: [
                    {}
                ],
                newTask: ''
            }
        },
        methods: {
            addTask() {
                this.tasks.push(newTask)
            }
        }
    }
</script>
  
  <style scoped>
  
    form {
        display: flex;
        margin-bottom: 50px;
        height: 5em;
        width: 800px;
        min-width: 400px;
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

    form button {
        height: 100%;
        width: 25%;
        border: none;
        color: #fff;
        font-size: 1.5em;
        background-color: #333433;	
        border-radius: 0px 10px 10px 0px;
    }

    form button:hover {
        background-color: #262726;	
    }

    li {
        display: flex;
        margin-bottom: 20px;
        height: 5em;
        width: 800px;
        min-width: 400px;
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
  