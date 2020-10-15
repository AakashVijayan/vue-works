<template>
    <div id="todo-list-example" class="demo">
  <form v-on:submit.prevent="addNewTodo">
    <label for="new-todo">Add a todo</label>
    <input
      v-model="newTodoText"
      id="new-todo"
      placeholder="E.g. Feed the cat"
    />
    <button @click="addItem"> Add</button>
    <button @click="clearItem"> Clear</button>
  </form>
  <ul>
    <li v-for="todo in todos" :key="todo.id">
        {{todo.title}}
    </li>
  </ul>

  <div>
    <p>Button click Events</p>
    <button @click="buttonClickCount++">
      You clicked me {{ buttonClickCount }} times.
    </button>

  </div>
</div>
</template>

<script>
export default {
    name:"Form",
    data(){
        return{
          buttonClickCount: 0,
             newTodoText: '',
      todos: [
        {id: 1, title: 'Do the dishes' },
        {id: 2, title: 'Take out the trash'},
        {id: 3, title: 'Mow the lawn'}
      ],
      nextTodoId: 4
        }
     
    },
   
    methods:{
        addItem(){
            this.todos.push({
        id: this.nextTodoId++,
        title: this.newTodoText
            }),
            this.newTodoText= ''
        },
        clearItem(){
      this.todos.pop({
        id: this.nextTodoId--,
        title: this.newTodoText =''
      })
      }
    }
}
</script>

<style>
.demo {
  font-family: sans-serif;
  border: 1px solid #eee;
  border-radius: 2px;
  padding: 20px 30px;
  margin-top: 1em;
  margin-bottom: 40px;
  user-select: none;
  overflow-x: auto;
}
</style>