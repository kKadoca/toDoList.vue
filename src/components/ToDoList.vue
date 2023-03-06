<template>
    <div>
        <form @submit.prevent="addTask">
            <input type="text" v-model="newTask.label">
            <button type="submit">Add task</button>
        </form>
        <ul :class="{hidden: !tasks.length}">
			<li v-for="(task, index) in tasks" :class="{completed: task.completed}" :key="index">
				<p> {{ task.label }}</p>
				<button class="green" @click="completeTask(task)">
                    <img src="../assets/complete-icon.png" alt="Complete Task">
                </button>
				<button class="red" @click="deleteTask(index)">
                    <img src="../assets/trash-icon.png" alt="Cancel Task">
                </button>
			</li>
		</ul>
        <button :class="{deactivated: !tasks.length}" @click="clearList()">
            Clear
        </button>
    </div>	
</template>
  
<script>
    export default {
        data() {
            return {
                tasks: [],
                newTask: {
                    label: ''
                }
            }
        },
        methods: {
            addTask() {
                if(this.newTask.label.trim() != '') {
                    this.tasks.push({
                        label: this.newTask.label,
                        completed: false
                    });
                    this.newTask = {
                        label: ''
                    };
                }
                else {
                    alert('Invalid Input')
                }
            },
            completeTask(task) {
                task.completed = true;
            },
            deleteTask(index) {
                this.tasks.splice(index, 1);
            },
            updateList() {
                // reorganizar as concluidas para o fim da lista
            },
            clearList() {
                this.tasks = [];
            }
        }
    }
</script>
  
  <style scoped>

    div {
        min-width: 350px;
        width: 75%;
        max-width: 800px;
    }
  
    form {
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 40px;
        flex-wrap: wrap;
        width: 100%;
        margin-bottom: 50px;
    }

    input {
        font-size: 2em;
        height: 3em;
        width: 72%;
        border: none;	
        border-radius: 10px;
        text-indent: 0.5em;
        color: #16161663;
        box-shadow: 3px 3px 10px #0000003f;
    }

    input:focus {
        color: #333433;
        outline: none;
    }

    button {
        height: 2em;
        width: 150px;
        border: none;
        color: #333433;
        font-size: 1.5em;
        background-color: #F2903E;	
        border-radius: 10px;
        box-shadow: 3px 3px 10px #0000003f;
    }

    button:hover {
        background-color: #333433;
        color: #F2913D;
        transition: .2s;
    }

    ul {
        display: flex;
        flex-direction: column;
        gap: 20px;
        width: 100%;
        margin-bottom: 40px;
    }

    li {
        display: flex;
        justify-content: space-around;
        align-items: center;
        height: max-content;
        width: 100%;
        padding: 15px;
        background-color: #fff;
        border-radius: 10px;
        box-shadow: 3px 3px 10px #0000003f;
    }

    p {
        text-align: start;
        font-size: 2em;
        height: 70%;
        width: 70%;
    }

    li button {
        height: 50px;
        width: 50px;
        border-radius: 25px;
        border: none;
        box-shadow: 3px 3px 10px #0000003f;
    }

    li img {
        margin-top: 6px;
        height: 60%;
        opacity: 0.5;
    }
    .green,
    .green:hover {
        background-color: #8af48a;
    }
    .red,
    .red:hover {
        background-color: #fb8181;
    }
    .completed p {
        text-decoration: line-through;
        color: #16161663;
        width: 95%;
    }
    .completed button {
        display: none;
    }

    .hidden {
        display: none;
    }

    .deactivated,
    .deactivated:hover {
        background-color: #d6d6d6;
        color: #838383;
    }

  </style>
  