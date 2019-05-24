<template>
<div>
<b-list-group v-bind:key="task.id" v-for="task in tasks">
    <app-task :task="task"></app-task>
</b-list-group>
</div>
</template>
<script>
import Task from './task.vue'
export default {
    name: 'Tasks',
    props:["tasks"],
    components:{
        'app-task': Task
    }
}
</script>

