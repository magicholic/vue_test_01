<script setup>
import { inject } from 'vue'
const parentValue = inject('parentValue')
</script>

<template>
  <div>
    <h2>Injected Value: {{ parentValue }}</h2>
  </div>
</template>
