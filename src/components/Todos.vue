<template>
  <div>
    <ol v-bind:key="todo.id" v-for="todo in todos">
      <Todo v-bind:todo="todo"/>
    </ol>
  </div>
</template>

<script>
import Todo from "./Todo.vue";
export default {
  name: "Todods",
  props: ["todos"],
  data: function() {
    return {};
  },
  components: { Todo }
};
</script>

<style scoped>
</style>