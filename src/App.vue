<template>
  <div class="wrapper">
    <my-header></my-header>
    <my-form @add="addTodo"></my-form>
    <my-todos></my-todos>
  </div>
</template>

<script>
import MyHeader from "./components/MyHeader.vue";
import MyForm from "./components/MyForm.vue";
import MyTodos from "./components/MyTodos.vue";
export default {
  components: {
    MyHeader,
    MyForm,
    MyTodos,
  },
  methods: {
    addTodo(todo) {
      console.log(todo);
    },
  },
};
</script>

<style>
/* Обнуление */
*,
*::before,
*::after {
  padding: 0;
  margin: 0;
  border: 0;
  box-sizing: border-box;
}

a {
  text-decoration: none;
}

ul,
ol,
li {
  list-style: none;
}

img {
  vertical-align: top;
}

html,
body {
  height: 100%;
}

body {
  background-color: #262336;
  font-family: Verdana, sans-serif;
  color: #fff;
}
.wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  width: 500px;
  margin: 0 auto;
}
</style>