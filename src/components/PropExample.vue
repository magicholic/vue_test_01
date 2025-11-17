<script setup>
const props = defineProps({
  msg: {
    type: String,
  },
})
</script>

<template>
  <div>
    <p>This is the message</p>
    <p>{{ msg }}</p>
  </div>
</template>
