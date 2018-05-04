<template>
  <div class="todoform w3-container w3-border w3-border-grey w3-center w3-padding">
    <input 
    type="text" 
    class="w3-input w3-border w3-half w3-margin w3-large" 
    v-model="newTodo" 
    @keyup.enter="addTodo">
      
    <button 
    class="w3-button w3-green w3-round w3-margin w3-large" 
    @click="addTodo">
    Add todo</button>

    <p class="w3-center w3-text-grey">{{newTodo}}</p>
  </div>
</template>

<script>
export default {
  data () {
    return {
      newTodo: ''
    }
  },
  methods: {
    addTodo () {
      if(this.newTodo) {
        this.$emit('addedTodo', this.newTodo);
        this.newTodo= '';
      }
    }
  }
}
</script>

<style>

</style>
