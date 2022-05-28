<template>
  <div>
    <form class="form">
      <p>Create a list if tasks :</p>
      <div>
        <my-input></my-input>
        <my-button class="button-form">Add</my-button>
      </div>
    </form>
  </div>
</template>

<script>
export default {};
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
}
</style>