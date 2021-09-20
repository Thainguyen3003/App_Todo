<template>
  <div id="app">
    <Task v-for="(task, index) in tasks" :key="index" :taskData="task" />
  </div>
</template>

<script>
import Task from './components/Task.vue'

export default {
  name: 'App',
  data() {
    return {
      tasks: [
        { content: 'di cho', done: false},
        { content: 'nau com', done: false},
        { content: 'an uong', done: false},
        { content: 'di ngu', done: false}
      ]
    }
  },
  components: {
    Task
  }


  /*
  mounted() {
    // goi API 
  },

  methods: {
    addTask: function() {
      this.tasks.push({
        content: this.newTask,
        done: false
      })
    },
  },
  watch: {
    newTask: function(newValue,oldValue) {
      console.log('new = ' + newValue);
      console.log('old = ' + oldValue);
    }
  }
  */
  

}

</script>

<style>
.done {
  text-decoration: line-through;
}

</style>
