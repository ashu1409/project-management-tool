<template>
  <div>
    <p>Are you sure you want to delete this task?</p>
    <button @click="confirmDelete">Yes</button>
    <button @click="cancelDelete">No</button>
  </div>
</template>

<script>
export default {
  methods: {
    confirmDelete() {
      // Emit an event to parent component to confirm deletion
      this.$emit('confirm-delete');
    },
    cancelDelete() {
      // Emit an event to parent component to cancel deletion
      this.$emit('cancel-delete');
    }
  }
};
</script>

<style>
/* Add your component styles here */
</style>
