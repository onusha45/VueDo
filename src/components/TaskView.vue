<template>
    <h2>{{ tasks }}</h2>
</template>

<script setup lang="ts">
defineProps({
  tasks: {
    type: Array
  }
})
</script>