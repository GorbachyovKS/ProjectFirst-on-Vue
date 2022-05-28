<template>
  <div>
    <form class="form">
      <p>Create a list if tasks :</p>
      <div>
        <input type="text" placeholder="Add a new task" class="input-form" />
        <button class="button-form">Add</button>
      </div>
    </form>
  </div>
</template>

<script>
export default {};
</script>

<style>
.form {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  padding-bottom: 30px;
}

.input-form {
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

.button-form {
  padding: 8px 20px;
  font-weight: 600;
  font-size: 1.3rem;
  border-radius: 10px;
  text-transform: uppercase;
}
</style>