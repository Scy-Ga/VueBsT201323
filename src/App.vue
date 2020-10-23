<template>
  <div id="app">

    <b-container>
      <b-row>
        <b-con>
          <label>Lehetséges Variációk</label>
        </b-con>
      </b-row>
      <b-row>
        <b-con>
          <jobSelectModal />
        </b-con>
      </b-row>
      <b-row><b-con><br></b-con></b-row>
      <b-row>
        <b-con>
          <jobSelectButton />
        </b-con>
      </b-row>
    </b-container>

    
    <br>
    

  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import HelloWorld from "./components/HelloWorld.vue";
import jobSelectModal from "./components/jobSelectModal.vue";
import jobSelectButton from "./components/jobSelectButton.vue";

@Component({
  components: {
    HelloWorld,
    jobSelectModal,
    jobSelectButton,
  },
})
export default class App extends Vue {

}


</script>

<style>
</style>
