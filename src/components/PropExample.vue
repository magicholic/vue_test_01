<script setup>
const props = defineProps({
  msg: {
    type: String,
  },
})
</script>

<template>
  <div>
    <h1>Prop logic</h1>
    <p>This is the message</p>
    <p>{{ msg }}</p>
  </div>
</template>
