<template>
    <div>
        <b-list-group-item>
            <b-row>
              <b-col cols="10">{{task.text}}</b-col> 
              <b-col cols="2"><b-button pill variant="outline-danger" @click="$emit('del-task', task.id)" size="sm">X</b-button></b-col>
            </b-row>
        </b-list-group-item>
    </div>
</template>
<script>
export default {
    name: 'Task',
    props:["task"]
}
</script>

