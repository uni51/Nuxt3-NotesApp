<script setup lang="ts">
const notesInput = reactive({
  title: "",
  note: "",
});
</script>

<template>
  <NCard class="card">
    <input class="input" placeholder="My title" v-model="notesInput.title" />
    <textarea class="input" placeholder="My note" v-model="notesInput.note" />
    <NButton> Save Note </NButton>
  </NCard>
</template>

<style scoped>
.card {
  padding: 1.5rem;
  display: flex;
  flex-direction: column;
}

.input {
  border: 0.1rem solid rgba(0, 0, 0, 0.1);
  margin-bottom: 0.5rem;
  border-radius: 0.25rem;
}
</style>
