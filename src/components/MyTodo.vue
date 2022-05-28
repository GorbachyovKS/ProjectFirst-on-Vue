<template>
  <div class="todos" :class="{ done: isDone, delete: isDelete }">
    <div>{{ todo.name }}</div>
    <div class="buttons">
      <my-button
        class="btn-done btn-todos"
        @click="made(), $emit('doneTodo', todo)"
        >Done</my-button
      >
      <my-button
        class="btn-delete btn-todos"
        @click="remove(), $emit('deleteTodo', todo)"
        >Delete</my-button
      >
    </div>
  </div>
</template>

<script>
export default {
  props: {
    todo: {
      type: Object,
      required: true,
    },
  },
  data() {
    return {
      isDone: false,
      isDelete: false,
    };
  },
  methods: {
    made() {
      this.isDone = true;
    },
    remove() {
      this.isDelete = true;
    },
  },
};
</script>

<style scoped>
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

.todos {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #342f4f;
  padding: 15px;
  border-radius: 15px;
  margin: 15px 0;
  transition: all 1s ease-in;
}

.done {
  background-color: #32d56f87;
  transform: translateX(-1000px);
}

.delete {
  background-color: #d6153f87;
  transform: translateX(-1000px);
}
</style>