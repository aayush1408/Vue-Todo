<template>
    <div>
      <p>Completed task: {{  todos.filter((todo) => { return todo.done===true }).length }}</p>
      <p>Incompleted task: {{ todos.filter((todo) =>{return todo.done===false}).length }}</p>
    </div>
</template>

<script type="text/javascript">
    export default{
        props:['todos']
    };
</script>

<style type="text/css">
    
</style>
