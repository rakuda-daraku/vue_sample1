<template>
  <div>
    <todo v-on:delete-todo="deleteTodo" v-for="(todo, index) in todos" v-bind:todo="todo" :key="index"></todo>
  </div>
</template>

<script type="text/javascript">
  import Todo from "./Todo";

  export default {
    props:['todos'],
    components: {
      Todo,
    },
    methods: {
      deleteTodo(todo) {
        const todoIndex = this.todos.indexOf(todo);
        this.todos.splice(todoIndex, 1);
      }
    }
  };
</script>
<style>
</style>
