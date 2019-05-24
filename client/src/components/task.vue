<template>
    <div>
          <b-list-group-item>{{task.text}}</b-list-group-item>
    </div>
</template>
<script>
export default {
    name: 'Task',
    props:["task"]
}
</script>

