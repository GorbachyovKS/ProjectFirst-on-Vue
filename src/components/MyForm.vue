<template>
  <div>
    <form class="form">
      <p>Create a list if tasks :</p>
      <div>
        <my-input v-model="todo.name" placeholder="Add a new task"></my-input>
        <my-button class="button-form" @click.prevent="addTodo">Add</my-button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      todo: {
        name: "",
      },
    };
  },
  methods: {
    addTodo() {
      if (this.todo.name) {
        this.todo.id = Date.now();
        this.$emit("add", this.todo);
        this.todo = {
          name: "",
        };
      }
    },
  },
};
</script>

<style scoped>
.form {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  padding-bottom: 30px;
}

.button-form {
  background-color: #32d56f;
  font-size: 1.3rem;
  font-weight: 600;
}
</style>