<template>
  <div class="wrapper">
    <my-header></my-header>
  </div>
</template>

<script>
import MyHeader from "./components/MyHeader.vue";
export default {
  components: {
    MyHeader,
  },
};
</script>

<style>
body {
  background-color: #262336;
  font-family: Verdana, sans-serif;
  color: #fff;
}
.wrapper {
  display: flex;
  justify-content: center;
}
</style>