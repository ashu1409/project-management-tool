<template>
  <form @submit.prevent="handleSubmit">
    <input v-model="title" type="text" placeholder="Task Title" required>
    <select v-model="status">
      <option value="pending">Pending</option>
      <option value="completed">Completed</option>
    </select>
    <input v-model="attachment" type="file">
    <button type="submit">Submit</button>
  </form>
</template>

<script>
export default {
  props: {
    task: {
      type: Object,
      default: null
    }
  },
  data() {
    return {
      title: this.task ? this.task.title : '',
      status: this.task ? this.task.status : 'pending',
      attachment: null
    };
  },
  methods: {
    handleSubmit() {
      const formData = new FormData();
      formData.append('title', this.title);
      formData.append('status', this.status);
      formData.append('attachment', this.attachment);

      // Make API call to add/edit task
      // Use Axios or Vue Resource for HTTP requests
      // Example: axios.post('/api/tasks', formData)
    }
  }
};
</script>

<style>
/* Add your component styles here */
</style>
