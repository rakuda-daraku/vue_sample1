<template>
  <div id="app">
    <todo-list v-bind:todos="todos"/>
    <create-todo v-on:add-todo="addTodo"/>
  </div>
</template>

<script>
  import TodoList from './components/TodoList'
  import CreateTodo from './components/CreateTodo'

  export default {
    name: 'app',
    components: {
      TodoList,
      CreateTodo
    },
    data() {
      return {
        todos:[
          {
            title: 'Todo A',
            project: 'Project A',
            done: false
          },
          {
            title: 'Todo B',
            project: 'Project B',
            done: true
          },
          {
            title: 'Todo C',
            project: 'Project C',
            done: false
          },
          {
            title: 'Todo D',
            project: 'Project D',
            done: false
          }
        ]
      }
    },
    methods: {
      addTodo(title) {
         this.todos.push({
           title,
           done: false
         });
      }
    }
  }
</script>

<style>
</style>
