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