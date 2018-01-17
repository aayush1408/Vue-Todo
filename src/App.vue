<template>
  <div id="app">
    <todo-list v-bind:todos="todos"></todo-list> 
  </div>
</template>
import TodoList from './components/TodoList.vue';

<script>
import TodoList from './components/TodoList.vue';
export default {
  
  components:{
    TodoList
  },
  
  data(){
    return{
      todos: [{
        title: 'Todo A',
        project: 'Project A',
        done: false,
      }, {
        title: 'Todo B',
        project: 'Project B',
        done: true,
      }, {
        title: 'Todo C',
        project: 'Project C',
        done: false,
      }, {
        title: 'Todo D',
        project: 'Project D',
        done: false,
      }]
    }
  }


}
</script>

<style>
#app {

}
</style>
