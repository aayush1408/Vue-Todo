<template>
  <div id="app">
    <todo-list v-bind:todos="todos"></todo-list> 
    <create-todo v-on:create-todo="createTodo"></create-todo>
  </div>
</template>
import TodoList from './components/TodoList.vue';
import CreateTodo from './components/CreateTodo.vue';
<script>
import TodoList from './components/TodoList.vue';
import CreateTodo from './components/CreateTodo.vue';
export default {
  
  components:{
    TodoList,
    CreateTodo
  },
  
  data(){
    return{
      todos: [{
        title: 'Todo A',
        project: 'Project A',
        done: false
      }, {
        title: 'Todo B',
        project: 'Project B',
        done: true
      }, {
        title: 'Todo C',
        project: 'Project C',
        done: false
      }, {
        title: 'Todo D',
        project: 'Project D',
        done: false
      }]
    }
  },
  methods: {
     createTodo(newTodo) {
      this.todos.push(newTodo);
    }
    }
  }



</script>

<style>
#app {

}
</style>
