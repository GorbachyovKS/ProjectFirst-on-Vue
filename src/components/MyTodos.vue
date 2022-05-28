<template>
  <div class="my-todos">
    <my-todo
      v-for="todo in todos"
      :key="todo.id"
      :todo="todo"
      @doneTodo="$emit('doneTodo', todo)"
      @deleteTodo="$emit('deleteTodo', todo)"
    ></my-todo>
  </div>
</template>

<script>
import MyTodo from "./MyTodo.vue";
export default {
  components: { MyTodo },
  props: {
    todos: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style scoped>
.my-todos {
  width: 100%;
}
</style>