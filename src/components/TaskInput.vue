<template>
  <div>
    <input type="text" v-model="task" />
    <button @click="addTask">Add task</button>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const emit = defineEmits(['add:task'])

const task = ref("")

function addTask() {
  emit("add:task", task)
}

</script>