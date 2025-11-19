<script setup>
import PageOne from './RoutesComps/PageOne.vue';
import PageTwo from './RoutesComps/PageTwo.vue';
import PageThree from './RoutesComps/PageThree.vue';
import { ref } from 'vue';

const currentPage = ref(PageOne); // Default to PageOne, currentPage is a component reference not a string
const pageChange = (pageComponent) => {
  currentPage.value = pageComponent;
};
</script>

<template>
  <div>
    <div>
      <a class="btn btn-sm btn-outline-primary" href="javascript://" @click="pageChange(PageOne)">Page One</a>
      <a class="btn btn-sm btn-outline-primary" href="javascript://" @click="pageChange(PageTwo)">Page Two</a>
      <a class="btn btn-sm btn-outline-primary" href="javascript://" @click="pageChange(PageThree)">Page Three</a>
    </div>
    <div>
      <component :is="currentPage" />
    </div>
  </div>
</template>

<style scoped>
a {
  margin-right: 5px;
}
</style>
