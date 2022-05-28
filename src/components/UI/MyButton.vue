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

<style>
.btn {
  padding: 8px 20px;
  font-weight: 600;
  font-size: 1.3rem;
  border-radius: 10px;
  text-transform: uppercase;
}
</style>