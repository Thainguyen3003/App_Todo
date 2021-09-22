<template>
  <div id="app" class="container">
    <img src="./assets/logo.png" alt="" class="logo">

    
    <Todolist />
    
    
  </div>
</template>

<script>
import Todolist from './components/Todolist.vue'
//import TagSelector from './components/TagSelector.vue'

export default {
  name: 'App',
  data() {
    return {
      tongTien: 1000000
    }
  },
  filters: {
    dauChamPhanTach: function (soTien) {
      return soTien.toFixed(2).replace(/\d(?=(\d{3})+\.)/g, '$&,');
    }
  },
  components: {
    Todolist,
    //TagSelector
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
* {
  box-sizing: border-box;
}

.container {
  max-width: 600px;
  margin: 0 auto;
}

#app {
  font-family: 'Avenir', Arial, Helvetica, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}

.logo {
  display: block;
  margin: 20px auto;
  height: 75px;
}

</style>
