<template>
  <div id="app">
    <Header />
    <Todos v-bind:todos="todos" v-on:del-todo="delelteTodo" />
  </div>
</template>

<script>
import uuid from "uuid";
import Header from "./components/layout/Header.vue";
import Todos from "./components/Todos.vue";
// import AddTodo from "./components/Addtodo.vue";
export default {
  name: "app",
  data: function() {
    return {
      message: "Hello World",
      todos: [
        {
          id: uuid(),
          title: "My First and Last TODO in Vue",
          complelted: false
        }
      ]
    };
  },
  components: {
    Header,
    Todos
  },
  methods: {
    delelteTodo(id) {
      console.log("deleting todo");
    }
  },
  addTodo(newToDo) {
    console.log("adding new todo");
  },
  created() {
    console.log("created");
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
