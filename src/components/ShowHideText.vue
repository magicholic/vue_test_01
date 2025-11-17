<script setup>
import { ref } from 'vue'

const textDisplay = ref(false)
const btnText = ref('Show Text')
function showText() {
  if (textDisplay.value === false) {
    textDisplay.value = true
    btnText.value = 'Hide Text'
  } else {
    textDisplay.value = false
    btnText.value = 'Show Text'
  }
}
function displayClass() {
  return textDisplay.value ? 'visible-text' : 'hidden-text'
}
</script>

<template>
  <div id="display-text">
    <button @click="showText" class="btn btn-sm btn-outline-primary">{{ btnText }}</button>
    <p v-if="textDisplay" :class="displayClass()" class="text-primary">This is the message</p>
  </div>
</template>
