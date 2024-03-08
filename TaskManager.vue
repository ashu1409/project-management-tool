<template>
  <div>
    <task-list :tasks="tasks" @edit-task="editTask" @delete-task="confirmDelete"></task-list>
    <task-form v-if="editingTask" :task="editingTask" @submit="saveTask"></task-form>
    <task-delete v-if="deletingTask" @confirm-delete="deleteTask" @cancel-delete="cancelDelete"></task-delete>
  </div>
</template>

<script>
import TaskList from './TaskList.vue';
import TaskForm from './TaskForm.vue';
import TaskDelete from './TaskDelete.vue';

export default {
  components: {
    TaskList,
    TaskForm,
    TaskDelete
  },
  data() {
    return {
      tasks: [],
      editingTask: null,
      deletingTask: null
    };
  },
  created() {
    // Fetch tasks from backend API
    // Example: axios.get('/api/tasks').then(response => this.tasks = response.data);
  },
  methods: {
    editTask(task) {
      this.editingTask = task;
    },
    saveTask(taskData) {
      // Make API call to save task
      // Example: axios.put(`/api/tasks/${taskData.id}`, taskData)
      this.editingTask = null;
    },
    confirmDelete(taskId) {
      this.deletingTask = taskId;
    },
    deleteTask() {
      // Make API call to delete task
      // Example: axios.delete(`/api/tasks/${this.deletingTask}`)
      this.deletingTask = null;
    },
    cancelDelete() {
      this.deletingTask = null;
    }
  }
};
</script>

<style>
/* Add your component styles here */
</style>
