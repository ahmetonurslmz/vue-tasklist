<template>
    <div>
       <form @submit="createTask">
          <b-row>
            <b-col cols="9">
         <b-form-input v-model="text" placeholder="enter task title" style="margin-bottom: 20px"></b-form-input>
          </b-col>
          <b-col cols="3">
            <b-button type="submit">Create Task</b-button>
          </b-col>
          </b-row>
            </form>
    </div>
</template>
<script>
import uid from 'uid'
export default {
    data() {
      return {
        text: ''
      }
    },
    methods: {
      createTask(e) {
            e.preventDefault()
            const newTask = {
              id: uid(10),
              text: this.text,
              state: false
            }
            this.$emit('create-task', newTask)
      }
    }

}
</script>

