<template>
  <div class="todos">
    <div>{{ todo.name }}</div>
    <div class="buttons">
      <my-button class="btn-done btn-todos">Done</my-button>
      <my-button class="btn-delete btn-todos">Delete</my-button>
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
</style>