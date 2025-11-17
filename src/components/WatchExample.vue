<script setup>
import { ref, watch } from 'vue'

// watch example
const watchedValue = ref(1)
watch(watchedValue, (newValue, oldValue) => {
  console.log('Old value - ' + oldValue)
  console.log('New value - ' + newValue)
  if (newValue > 5) {
    console.log('Value exceeded 5')
  }
})
</script>

<template>
  <div id="watchExample">
    <h1>Watch Example:</h1>
    <p>Watched Value: {{ watchedValue }}</p>
    <button @click="watchedValue++" class="btn btn-sm btn-outline-primary">
      Increase Watched Value</button
    ><br />
    <button
      @click="watchedValue > 0 ? watchedValue-- : watchedValue"
      class="btn btn-sm btn-outline-secondary"
    >
      Decrease Watched Value
    </button>
  </div>
</template>
