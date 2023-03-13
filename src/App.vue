<template>
  <!-- Temporal Nav Bar, It's just a reference -->
  <div id="navBar"></div>
  <!-- <BaseTable></BaseTable> -->
  <BaseViewer></BaseViewer>
  <Footer></Footer>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import BaseTable from './components/Table/BaseTable.vue';
import BaseViewer from './components/Viewer/BaseViewer.vue';
import Footer from './components/Footer.vue';


export default {
  components: {
    BaseTable,
    BaseViewer,
    Footer
}
};
</script>

<style>
/* Temporal Nav Bar, It's just a reference */
#navBar {
  height: 50px;
  width: 100%;
  box-shadow: 0px 3px 7px rgba(0, 0, 0, 0.2);
  background-color: var(--primary-soft-color);
}
</style>
