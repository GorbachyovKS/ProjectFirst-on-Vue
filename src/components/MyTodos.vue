<template>
  <div class="my-todos">
    <div class="todos" v-for="todo in todos" :key="todo.id">
      <div>{{ todo.name }}</div>
      <div class="buttons">
        <my-button class="btn-done btn-todos">Done</my-button>
        <my-button class="btn-delete btn-todos">Delete</my-button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    todos: {
      type: Array,
      required: true,
    },
  },
  data() {
    return {
      todos: [
        { id: 1, name: "Hello" },
        { id: 2, name: "my" },
        { id: 3, name: "App" },
      ],
    };
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
.btn-done {
  background-color: #32d56f;
}

.btn-delete {
  background-color: #d6153f;
  color: #fff;
}

.btn-todos {
  font-size: 0.9rem;
  font-weight: 600;
}

.buttons {
  display: flex;
  gap: 15px;
}
</style>