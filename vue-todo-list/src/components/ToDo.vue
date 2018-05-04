<template>
  <div class="todo w3-container w3-center">
    <label>{{index + 1}}.- {{todo.title}}</label>
    <input class="w3-check" type="checkbox" v-model="todo.completed">
    <hr>
  </div>
</template>

<script>
export default {
  props: {
    todo: {
      type: Object,
      required: true
    },
    index: {
      type: Number,
      required: true
    }
  }
}
</script>

<style scoped>

</style>
