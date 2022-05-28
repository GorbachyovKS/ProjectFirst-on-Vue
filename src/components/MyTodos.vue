<template>
  <div class="my-todos">
    <my-todo v-for="todo in todos" :key="todo.id" :todo="todo"></my-todo>
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
.todos {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #342f4f;
  padding: 15px;
  border-radius: 15px;
  margin: 15px 0;
}
</style>