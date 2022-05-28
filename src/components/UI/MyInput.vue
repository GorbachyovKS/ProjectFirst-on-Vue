<template>
  <input :value="modelValue" @input="updateInput" type="text" class="input" />
</template>

<script>
export default {
  name: "my-input",
  props: {
    modelValue: [String, Number],
  },
  methods: {
    updateInput(event) {
      this.$emit("update:modelValue", event.target.value);
    },
  },
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