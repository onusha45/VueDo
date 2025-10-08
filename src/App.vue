<template>
 <div class="todo">
  <h1>Todo App</h1>

  <TaskInput @add:task="addTask" />

  <TaskView :tasks="tasks" />
 </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import TaskInput from './components/TaskInput.vue';
import TaskView from './components/TaskView.vue';

const tasks = ref(["apple", "mango"])

function addTask(task: string) {
  tasks.value.push(task)
}
</script>

<style>
.todo h1 {
  text-align: center;
  margin-bottom: 2rem;
}
</style>


 