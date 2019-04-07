<template>
  <div id="app">
    <Todos v-bind:todos="todos" v-on:del-todo="delToDo"/>
  </div>
</template>
 
<script>
import Todos from './components/ToDos'; 

export default {
  name: 'app',
  components: {
    Todos
  },
  data() {
    return {
      todos: [
        {
          id: 1,
          title: "ToDo 1",
          completed: false
        },
        {
          id: 2,
          title: "ToDo 2",
          completed: true
        },
        {
          id: 3,
          title: "ToDo 3",
          completed: false
        }
      ]
    }
  },
  methods: {
    delToDo(id){
      this.todos = this.todos.filter(todo => todo.id !== id);
    }
  }
}
</script>

<style>
  *{
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  body {
    font-family: Arial, Helvetica, sans-serif;
    line-height: 1.4;
  }
</style>
