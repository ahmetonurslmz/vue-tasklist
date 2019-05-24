<template>
  <div id="app">
    <b-container>
      <b-row align-h="center">
        <b-col cols="6">
           <app-addTask v-on:create-task="createTask"></app-addTask>
           <app-tasks :tasks="tasks"></app-tasks>
        </b-col>
      </b-row>
    </b-container>

  </div>
</template>

<script>
//Boostrap Files
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'

//Components
import addTask from './components/addTask.vue'
import Tasks from './components/tasks.vue'

export default {
  name: 'app',
  components: {
    'app-addTask': addTask,
    'app-tasks': Tasks
  },
  data() {
    return {
      tasks: [],
    }
  },
  created() {
    this.tasks=[ {
      id: 1,
      text: 'An Example of Task List Element',
      state: false
    }]
  },
  methods: {
    createTask(newTask) {
      this.tasks.unshift({...newTask})
    }
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
