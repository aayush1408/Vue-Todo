<template>
    <div>
      <p>Completed task: {{  todos.filter((todo) => { return todo.done===true }).length }}</p>
      <p>Incompleted task: {{ todos.filter((todo) =>{return todo.done===false}).length }}</p>
      <todo  v-on:delete-todo="deleteTodo" v-on:complete-todo="completeTodo" v-for="todo in todos" v-bind:todo="todo"  ></todo>
    </div>
</template>
import Todo from './Todo.vue';
<script type="text/javascript">
import Todo from './Todo.vue';

    export default{
        props:['todos'],
        components:{
          Todo
        },
        methods:{
          deleteTodo(todo) {
            const todoIndex = this.todos.indexOf(todo);
            this.todos.splice(todoIndex, 1);
          },
          completeTodo(todo) {
            const todoIndex = this.todos.indexOf(todo);
            this.todos[todoIndex].done = true;
        }
        }
    };
</script>

<style type="text/css">
    
</style>
