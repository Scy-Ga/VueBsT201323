<template>
  <div id="app">

    <jobSelectModal />

  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import HelloWorld from "./components/HelloWorld.vue";
import jobSelectModal from "./components/jobSelectModal.vue";

@Component({
  components: {
    HelloWorld,
    jobSelectModal,
  },
})
export default class App extends Vue {}
</script>

<style>
</style>
