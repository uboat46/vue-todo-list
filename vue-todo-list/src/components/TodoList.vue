<template>
  <div class="todolist">
    <header class="w3-bar w3-xlarge w3-blue">
      <div class="w3-bar-item">
        A Vue Simple Todo List
      </div>
    </header>

    <section class="w3-container w3-border w3-border-grey w3-center w3-padding">
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
    </section>

    <section class="w3-container w3-border w3-border-grey">
      <h2>ToDo´s</h2>
      <to-do 
      v-for="(todo, index) in todos" 
      :key="index"
      :todo="todo"
      :index="index"/>
    </section>

    <section class="w3-container w3-border w3-border-grey">
      <h3>Done</h3>
    </section>

  </div>
</template>

<script>
import ToDo from './ToDo'

export default {
  components: {
    ToDo
  },
  data () {
    return {
      newTodo: '',
      todos: []
    }
  },
  methods: {
    addTodo () {
      if(this.newTodo) {
        this.todos.push({
          title: this.newTodo,
          completed: false
        });
        this.newTodo= '';
      }
    }
  }
}
</script>

<style scoped>
.todolist {
  width: 100%;
  height: 100%;
}
</style>
