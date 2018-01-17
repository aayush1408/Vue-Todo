<template>
    <div>
      <p>Completed task: {{  todos.filter((todo) => { return todo.done===true }).length }}</p>
      <p>Incompleted task: {{ todos.filter((todo) =>{return todo.done===false}).length }}</p>
      <todo  v-for="todo in todos" v-bind:todo="todo"></todo>
    </div>
</template>
import Todo from './Todo.vue';
<script type="text/javascript">
import Todo from './Todo.vue';

    export default{
        props:['todos'],
        components:{
          Todo
        }
    };
</script>

<style type="text/css">
    
</style>
