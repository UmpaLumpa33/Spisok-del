<template>
  <div class="task-item">
    <h3>{{ task.title }}</h3>
    <p>{{ task.text }}</p>
  </div>
</template>

<script setup lang="ts">
defineProps({
  task: Object as PropType<ITask>,
})

interface ITask {
  id: number;
  title: string;
  text: string;
}
</script>

<style scoped>
.task-item {
  background-color: #fafafa;
  border-radius: 8px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
  padding: 16px;
  transition: transform 0.2s ease-in-out;
}

.task-item h3 {
  font-size: 1.2rem;
  margin-bottom: 8px;
  color: #333;
}

.task-item p {
  line-height: 1.5;
  color: #666;
}

.task-item:hover {
  transform: scale(1.02);
}
</style>