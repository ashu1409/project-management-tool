<template>
  <div>
    <h1>Task List</h1>
    <ul>
      <li v-for="task in tasks" :key="task.id">
        <span>{{ task.title }}</span>
        <span>{{ task.status }}</span>
        <button @click="editTask(task)">Edit</button>
        <button @click="deleteTask(task.id)">Delete</button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    tasks: {
      type: Array,
      required: true
    }
  },
  methods: {
    editTask(task) {
      // Emit an event to parent component to edit task
      this.$emit('edit-task', task);
    },
    deleteTask(taskId) {
      // Emit an event to parent component to delete task
      this.$emit('delete-task', taskId);
    }
  }
};
</script>

<style>
/* Add your component styles here */
</style>
