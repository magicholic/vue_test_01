<script setup>
import { ref } from 'vue'
const items = ref(['Item 1', 'Item 2', 'Item 3'])
</script>

<template>
  <div id="listItems">
    <h3>List of Items:</h3>
    <ul>
      <li v-for="(item, index) in items" :key="index">
        <a href="javascript://">
          {{ item }}
        </a>
      </li>
    </ul>
  </div>
</template>

<style scoped>
ul {
  padding: 0;
}
ul li {
  margin-bottom: 5px;
  list-style-type: none;
}
a {
  text-decoration: none;
  color: #007bff;
}
a:hover {
  text-decoration: underline;
}
</style>
