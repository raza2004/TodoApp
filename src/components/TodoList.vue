<template>
  <div class="TodoList">
    <form @submit.prevent="addTodo">
      <input class="todo-text" type="text" v-model="newTodo" placeholder="Add a new to-do" />
      <button type="submit">Add</button>
    </form>
    <ul class="ul">
      <li v-for="(todo, index) in todos" :key="todo.id" 
      
      >
        {{ todo.text }}
        <button class="remove" @click="removeTodo(index)">X</button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      todos: [],
      newTodo: ""
    };
  },
  methods: {
    addTodo() {
      this.todos.push({
        id: Date.now(),
        text: this.newTodo
      });
      this.newTodo = "";
    },
    removeTodo(index) {
      this.todos.splice(index, 1);
    }
  }
};
</script>
<style scoped>
.todo-item {
    display: flex;
    align-items: center;
    padding: 0.5em;
    /* background-color: #f4f4f4; */
    margin-bottom: 0.5em;
    
}

.todo-text {
    flex-grow: 1;
    margin-right: 0em;
}

.remove{
    background-color: #ff0000;
    color: #fff;
    border: none;
    padding: 0.5em;
    cursor: pointer;
}
.ul{
  padding: 2em;
}
</style>

