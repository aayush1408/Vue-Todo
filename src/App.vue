<template>
  <div id="app">
    <todo-list v-bind:todos="todos"></todo-list> 
    <create-todo v-on:create-todo="createTodo"></create-todo>
  </div>
</template>
import TodoList from './components/TodoList.vue';
import axios from 'axios';

import CreateTodo from './components/CreateTodo.vue';
<script>
import TodoList from './components/TodoList.vue';
import CreateTodo from './components/CreateTodo.vue';
import axios from 'axios';
export default {
  
  components:{
    TodoList,
    CreateTodo
  },
  
  data(){
    return{
      todos:[]
    }
  },
  beforeMount(){
      axios.get('http://localhost:5000/todos')
      .then(function (response) {
         this.todos.push(...response.data);
    }.bind(this))
    .catch(function (error) {
        console.log(error.message);
    });
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
