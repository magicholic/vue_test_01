<script setup>
const props = defineProps({ msg : String})
</script>

<template>
  <div>
    <h1>Prop logic</h1>
    <p>This is the message</p>
    <p>{{ props.msg }}</p>
  </div>
</template>
