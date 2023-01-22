<template>
  <img alt="Vue logo" src="./assets/logo.png">
 <TodoList/>
</template>

<script>
import TodoList from './components/TodoList.vue';


export default {
  name: 'App',
  components: {
    
    TodoList
}
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: justify;
  color: #2c3e50;
  margin-top: 60px;
  background-color: #bed0e2;
  color: rgb(6, 59, 41);
}
</style>
