<template>
  <button class="btn">
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: "my-button",
};
</script>

<style scoped>
.btn {
  padding: 8px 20px;
  border-radius: 10px;
  text-transform: uppercase;
}
</style>