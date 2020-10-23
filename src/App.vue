<template>
  <div id="app"></div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import HelloWorld from "./components/HelloWorld.vue";
import jobSelect from "./components/jobSelect.vue";

@Component({
  components: {
    HelloWorld,
    jobSelect,
  },
})
export default class App extends Vue {}
</script>

<style>
</style>
