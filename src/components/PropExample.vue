<script setup>
const props = defineProps({
  msg: {
    type: String,
  },
})
</script>

<template>
  <h1>Prop logic</h1>
  <div>
    <p>This is the message</p>
    <p>{{ msg }}</p>
  </div>
</template>
