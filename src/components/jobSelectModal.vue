<template>
  <div class="jobselect">
    <div>
      <b-button v-b-modal.modal-1 size="sm"
        >Folymatban lévő munka státusza</b-button
      >

      <b-modal
        id="modal-1"
        title="Munka Státusza"
        size="lg"
        centered
        header-text-variant="primary"
        header-bg-variant="light"
        body-bg-variant="light"
        footer-bg-variant="light"
      >
        <b-container>
          <b-row>
            <b-col><span>Státus:</span></b-col>
          </b-row>
          <b-row>
            <b-col>
              <b-form-select
                v-show="!status"
                v-model="munkaallapot"
                class="mb-3"
                size="md"
              >
                <b-form-select-option value="null"
                  >Please select</b-form-select-option
                >
                <b-form-select-option value="Folyamatban"
                  >Folyamatban</b-form-select-option
                >
                <b-form-select-option value="Ellenőrzésre"
                  >Ellenőrzésre</b-form-select-option
                >
                <b-form-select-option value="Átnézve"
                  >Átnézve</b-form-select-option
                >
                <b-form-select-option value="Eközmű"
                  >Eközmű</b-form-select-option
                >
                <b-form-select-option value="Engedély"
                  >Engedély</b-form-select-option
                >
                <b-form-select-option value="Kiküldve"
                  >Kiküldve</b-form-select-option
                >
                <b-form-select-option value="Lezárva"
                  >Lezárva</b-form-select-option
                >
              </b-form-select>
            </b-col>
          </b-row>
          <b-row>
            <b-col>
              <div class="form-group">
                <label>Megjegyzés(ek):</label>
                <textarea
                  v-model="comment"
                  class="form-control"
                  name="texArea"
                  id="tarea"
                  rows="3"
                ></textarea>
              </div>
            </b-col>
          </b-row>
        </b-container>
        <template v-slot:modal-footer>
          <div class="w-100">
            <b-button
              variant="success"
              size="sm"
              class="float-right m-1"
              @click="save"
              >Mentés</b-button
            >
            <b-button
              variant="primary"
              size="sm"
              class="float-right m-1"
              @click="modalshow = false"
              >Mégsem</b-button
            >
          </div>
        </template>
      </b-modal>
    </div>
  </div>
</template>


<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class jobSelect extends Vue {
  private get munkaallapot(): any {
    if (this.$store.state.nyekmunkakModules.__Editdata.status == undefined) {
      return null;
    } else {
      return this.$store.state.nyekmunkakModules.__Editdata.status;
    }
  }

  private get modalShow(): boolean {
    return this.$store.state.nyekmunkakModules.__showEditForm;
  }

  private set modalShow(value: boolean) {
    this.$store.state.nyekmunkakModules.__showEditForm = value;
  }

  private set munkaallapot(value: any) {
    this.$store.state.nyekmunkakModules.__Editdata.status = value;
  }

  private set comment(value: any) {
    this.$store.state.nyekmunkakModules.__Editdata.comment = value;
  }

  private save(): void {
    if (this.$store.state.nyekmunkakModules.__Editdata.status != null) {
      this.$store.state.nyekmunkakModules.__Editdata.status = this.munkaallapot;
    }

    if (this.$store.state.nyekmunkakModules.__Editdata.comment != null) {
      this.$store.state.nyekmunkakModules.__Editdata.comment = this.comment;
    }

    this.modalShow = false;
    this.$store.state.nyekmunkakModules.__new = false;
  }
}
</script>

<style>
</style>