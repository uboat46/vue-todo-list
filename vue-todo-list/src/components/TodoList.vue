<template>
  <div class="todolist">
    <header class="w3-bar w3-xlarge w3-blue">
      <div class="w3-bar-item">
        A Vue Simple Todo List
      </div>
    </header>

    <section class="w3-container w3-border w3-border-grey w3-center w3-padding">
      <to-do-form @addedTodo="addTodo"/>
    </section>

    <section class="w3-container w3-border w3-border-grey">
      <h2>ToDo´s</h2>
      <to-do 
      v-for="(todo, index) in uncompletedTodos" 
      :key="index"
      :todo="todo"
      :index="index"/>
    </section>

    <section class="w3-container w3-border w3-border-grey">
      <h2>Done</h2>
      <to-do 
      v-for="(todo, index) in completedTodos" 
      :key="index"
      :todo="todo"
      :index="index"/>
    </section>

  </div>
</template>

<script>
import ToDoForm from './ToDoForm'
import ToDo from './ToDo'

export default {
  components: {
    ToDoForm,
    ToDo
  },
  data () {
    return {
      todos: []
    }
  },
  methods: {
    addTodo (todo) {
      this.todos.push({
        title: todo,
        completed: false
      })
    }
  },
  computed: {
    completedTodos () {
      return this.todos.filter(todo => todo.completed);
    },
    uncompletedTodos () {
      return this.todos.filter(todo => !todo.completed);
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
