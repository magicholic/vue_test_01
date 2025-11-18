<script setup>
import { provide, ref } from 'vue'
import CounterLogic from './components/CounterLogic.vue'
import ColorChangeText from './components/ColorChangeText.vue'
import ShowHideText from './components/ShowHideText.vue'
import ListItems from './components/ListItems.vue'
import WatchExample from './components/WatchExample.vue'
import EmitExample from './components/EmitExample.vue'
import SlotExample from './components/SlotExample.vue'
import PropExample from './components/PropExample.vue'
import FirstComp from './components/FirstComp.vue'
import 'bootstrap/dist/css/bootstrap.min.css'
import 'bootstrap/dist/js/bootstrap.bundle.min.js'

const clickValue = ref(0)
const handleClick = () => {
  clickValue.value++
  console.log(`Button clicked ${clickValue.value} times`)
}
provide('parentValue', 1234)
</script>

<template>
  <div class="row">
    <div class="cell col-12 col-md-6 col-lg-4">
      <CounterLogic />
    </div>
    <div class="cell col-12 col-md-6 col-lg-4">
      <ColorChangeText />
    </div>
    <div class="cell col-12 col-md-6 col-lg-4">
      <ShowHideText />
    </div>
    <div class="cell col-12 col-md-6 col-lg-4">
      <ListItems />
    </div>
    <div class="cell col-12 col-md-6 col-lg-4">
      <WatchExample />
    </div>
    <div class="cell col-12 col-md-6 col-lg-4">
      <EmitExample @run-click="handleClick" />
    </div>
    <div class="cell col-12 col-md-6 col-lg-4">
      <SlotExample>
        <p>HHHHHHHHHXXXXXXXXXXXXXXXXXXXX.</p>
      </SlotExample>
    </div>
    <div class="cell col-12 col-md-6 col-lg-4">
      <SlotExample v-slot:header>header text</SlotExample>
    </div>
    <div class="cell col-12 col-md-6 col-lg-4">
      <PropExample msg="1234 - 1234++++" />
    </div>
    <div class="cell col-12 col-md-6 col-lg-4">
      <FirstComp />
    </div>
  </div>
</template>

<style>
button {
  margin-bottom: 5px;
  padding: 5px;
  width: 200px;
  border-radius: 10px;
}
.cell {
  height: 300px;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
