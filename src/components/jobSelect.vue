<template>
  <div class="jobselect">
      <div>
      <b-button v-b-modal.modal-1 size="sm">Folymatban lévő munka státusza</b-button>
      
      <b-modal id="modal-1" title="Munka Státusza" size="lg"> 

        <b-container>
          <b-row>
            <b-col><span>Státus:</span></b-col>
          </b-row>
          <b-row>
            <b-col>
              <b-form-select v-show="!status" v-model="munkaallapot" class="mb-3" size="md">
                <b-form-select-option value="null">Please select</b-form-select-option>
                <b-form-select-option value="Folyamatban">Folyamatban</b-form-select-option>
                <b-form-select-option value="Ellenőrzésre">Ellenőrzésre</b-form-select-option>
                <b-form-select-option value="Átnézve">Átnézve</b-form-select-option>
                <b-form-select-option value="Eközmű">Eközmű</b-form-select-option>
                <b-form-select-option value="Engedély">Engedély</b-form-select-option>
                <b-form-select-option value="Kiküldve">Kiküldve</b-form-select-option>
                <b-form-select-option value="Lezárva">Lezárva</b-form-select-option>
              </b-form-select>
            </b-col>
          </b-row>
          <b-row>
            <b-col>
              <div class="form-group">
                <label>Megjegyzés(ek):</label>
                <textarea class="form-control" name="texArea" id="tarea" rows="3"></textarea>
              </div>
            </b-col>
          </b-row>
        </b-container>
      </b-modal>
    </div>
  
     <div>
    <b-button id="show-btn" @click="showModal">Open Modal</b-button>
    <b-button id="toggle-btn" @click="toggleModal">Toggle Modal</b-button>

    <b-modal ref="my-modal" hide-footer title="Using Component Methods">
      <div class="d-block text-center">
        <h3>Hello From My Modal!</h3>
      </div>
      <b-button class="mt-3" variant="outline-danger" block @click="hideModal">Close Me</b-button>
      <b-button class="mt-2" variant="outline-warning" block @click="toggleModal">Toggle Me</b-button>
    </b-modal>
  </div>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class jobSelect extends Vue {
  
}
</script>

<style>

</style>