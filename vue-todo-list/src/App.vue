<template>
  <div id="app">
    <TodoList/>
  </div>
</template>

<script>
import TodoList from './components/TodoList'

export default {
  name: 'App',
  components: {
    TodoList
  }
}
</script>

<style>
@import url(./assets/w3.css);

html {
  height: 100%;
  width: 100%;
}

body {
  height: 100%;
  width: 100%;
}

#app {
  width: 100%;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
