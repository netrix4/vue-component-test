<script setup>
// const taskProp = defineProps(["taskTitle", "taskContent", "taskStyle"]);
const taskList = defineProps(["taskListProp"]);
</script>
<template>
  <div v-for="task in taskList.taskListProp">
    <div class="main-container" :style="task.style">
      <!-- <div :class="`main-container {${task.style}}`"> -->
      <div class="task-item">
        <h3>{{ task.title }}</h3>
        <p>Contenidooo {{ task.content }}</p>
      </div>
    </div>
  </div>
</template>
<style lang="css">
.main-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  justify-items: center;
  background-color: rgb(189, 90, 90);
  border: 10px;
  border-radius: 10px;
  padding: 3%;
  color: #fff;
}
</style>
