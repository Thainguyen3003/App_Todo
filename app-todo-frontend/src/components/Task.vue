<template>
  <div class="task">
    <span>{{ taskData.content}}</span>
  </div>
</template>

<script>
export default {
    props: {
      taskData: {
        type: String,
        default: function() { return {} }
      }
    },
  data() {
    return {
        content: 'abc',

    }
  },
  methods: {
      deleteTask: function() {
          console.log(this.taskData)
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
