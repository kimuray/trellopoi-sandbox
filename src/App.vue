<template>
  <div id="app">
    <draggable :options="{ group: 'tasks' }" element="ul" v-for="list in tasks">
      <li v-for="item in list">{{ item }}</li>
    </draggable>
  </div>
</template>

<script>
import draggable from 'vuedraggable';

export default {
  name: 'app',
  components: {
    draggable,
  },
  data() {
    return {
      tasks: [
        ['task1-1', 'task1-2', 'task1-3', 'task1-4'],
        ['task2-1', 'task2-2', 'task2-3', 'task2-4'],
        ['task3-1', 'task3-2', 'task3-3', 'task3-4']
      ]
    }
  }
}
</script>

<style>
#app {
  display: flex;
  justify-content: space-around;
}
ul {
  list-style: none;
  padding: 20px;
  margin: 20px;
  border: 1px solid #222;
}
li {
  cursor: pointer;
  padding: 10px;
  border: 1px solid #222;
  margin-bottom: 10px;
}
</style>
