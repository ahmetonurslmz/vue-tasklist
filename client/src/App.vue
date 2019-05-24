<template>
  <div id="app">
    <b-container>
      <b-row align-h="center">
        <b-col cols="6">
           <app-addToDo></app-addToDo>
           <app-tasks :tasks="tasks"></app-tasks>
        </b-col>
      </b-row>
    </b-container>

  </div>
</template>

<script>
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'
import addToDo from './components/addToDo.vue'
import Tasks from './components/tasks.vue'

export default {
  name: 'app',
  components: {
    'app-addToDo': addToDo,
    'app-tasks': Tasks
  },
  data() {
    return {
      tasks: [],
    }
  },
  created() {
    this.todolist=[ {
      text: 'An Example of Task List Element'
    }]
  }
}
</script>


<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
