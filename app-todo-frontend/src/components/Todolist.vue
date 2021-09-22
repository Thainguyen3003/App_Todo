<template>
  <div>
    <input type="text" class="todo-input" placeholder="What needs to be done" v-model="newTodo">
    <p>Todo list goes here</p>
    
    <div v-for="todo in todos" :key="todo.id" class="todo-item">
      {{ todo.title }}
    </div>
  </div>
</template>

<script>
export default {
  name: 'todo-list',
  data() {
    return {
      newTodo: '',
      idForTodo: 3,
      todos: [
        {
          'id': 1,
          'title': 'Finish Vue Screencast',
          'completed': false,
        },
        {
          'id': 2,
          'title': 'di cho',
          'completed': false,
        },
        {
          'id': 3,
          'title': 'Nau com',
          'completed': false,
        }
      ]
    }
  },
  methods: {
    addTodo() {
      this.todos.push({
        id: this.idForTodo,
        title: this.newTodo,
        completed: false,
      }) 
      
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .todo-input {
    width: 100%;
    padding: 10px 18px;
    font-size: 18px;
    margin-bottom: 16px;
  }
</style>
