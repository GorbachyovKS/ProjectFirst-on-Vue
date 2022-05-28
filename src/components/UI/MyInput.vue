<template>
  <input
    v-model="todo"
    type="text"
    placeholder="Add a new task"
    class="input"
  />
</template>

<script>
export default {
  name: "my-input",
};
</script>

<style scoped>
.input {
  max-width: 300px;
  margin: 30px 10px 0 0;
  outline: none;
  border: 0px;
  border-bottom: 1px solid white;
  background-color: transparent;
  text-align: left;
  font-size: 1.5rem;
  padding: 8px 20px 8px 0;
  color: #fff;
}
</style>