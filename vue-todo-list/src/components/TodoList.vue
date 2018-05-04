<template>
  <div class="todolist">
    <header class="w3-bar w3-xlarge w3-blue">
      <div class="w3-bar-item">
        A Vue Simple Todo List
      </div>
    </header>
    <section class="w3-container w3-border w3-border-grey w3-center w3-padding">
      <input type="text" class="w3-input w3-border w3-half w3-margin w3-large">
      <button class="w3-button w3-green w3-round w3-margin w3-large">Add todo</button>
    </section>
    <section class="w3-container w3-border w3-border-grey">
      <h3>ToDo´s</h3>
    </section>
    <section class="w3-container w3-border w3-border-grey">
      <h3>Done</h3>
    </section>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.todolist {
  width: 100%;
  height: 100%;
}
</style>
