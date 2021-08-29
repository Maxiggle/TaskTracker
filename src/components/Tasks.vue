<template>
  <div v-for="index in tasksArray" :key="index.id" >
    <Task @toggle-reminder="$emit('toggle-reminder', index.id)" @delete-task="$emit('delete-task',index.id)" :task="index" />
  </div>
</template>

<script>
import Task from "./Task";
export default {
  name: "Tasks",
  props: {
    tasksArray: Array,
  },
  components: {
    Task,
  },
  emits: ['delete-task','toggle-reminder'],
};
</script>

