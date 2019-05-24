<template>
    <div>
        <b-list-group-item>
            <b-row>
              <b-col cols="2"> <b-form-checkbox type="checkbox" @change="markComplete"></b-form-checkbox></b-col>
              <b-col cols="8" v-bind:class="{'task-text-completed': task.state }">{{task.text}}</b-col> 
              <b-col cols="2"><b-button pill variant="outline-danger" @click="$emit('del-task', task.id)" size="sm">X</b-button></b-col>
            </b-row>
        </b-list-group-item>
    </div>
</template>
<script>
export default {
    name: 'Task',
    props:["task"],
    methods: {
        markComplete() {
            this.task.state=!this.task.state
        }
    }
}
</script>

<style scoped>
.task-text-completed {
    text-decoration: line-through;
}
</style>
