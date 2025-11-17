<script setup>
import { ref } from 'vue'

// Color Change Functionality
const textClass = ref('text-danger')
const changeColor = () => {
  if (textClass.value === 'text-danger') textClass.value = 'text-primary'
  else textClass.value = 'text-danger'
}
</script>

<template>
  <div id="colorChangeSection">
    <div id="colorChangeBtn">
      <button @click="changeColor" class="btn btn-sm btn-outline-primary">
        Click to change color
      </button>
    </div>
    <div id="colorChangeTxt">
      <p :class="textClass">This should be red.</p>
    </div>
  </div>
</template>
