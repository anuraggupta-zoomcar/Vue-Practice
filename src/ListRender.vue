<template>
  <div v-for="(todo, index) in todoList" :key="index">
    <p>{{ todo.id }}</p>
    <p>{{ todo.title }}</p>
    <p>{{ todo.description }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      todoList: [
        { id: 1, title: "Title 1", description: "Description 1" },
        { id: 2, title: "Title 2", description: "Description 2" },
        { id: 3, title: "Title 3", description: "Description 3" },
        { id: 4, title: "Title 4", description: "Description 4" },
      ],
    };
  },
};
</script>

<style></style>
