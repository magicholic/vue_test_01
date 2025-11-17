<script setup>
import { computed, ref } from 'vue'

// counter Functionality
const counter = ref(1)
const increment = () => {
  counter.value++
}
const decrement = () => {
  if (counter.value > 0) {
    counter.value--
  }
}
const counterCheck = computed(() => {
  return counter.value > 4 ? counterMsg() : ''
})
function counterMsg() {
  return 'Now the number is larger than 4'
}
</script>

<template>
  <div id="counterSection">
    <h1>Counter Logic</h1>
    <div id="counterLogic">
      <button @click="increment" class="btn btn-sm btn-outline-primary">Increment Counter</button
      ><br />
      <button @click="decrement" class="btn btn-sm btn-outline-secondary">Decrement Counter</button>
      <p>Counter: {{ counter }}</p>
    </div>
    <div id="counterCheck">
      <p>{{ counterCheck }}</p>
    </div>
  </div>
</template>
