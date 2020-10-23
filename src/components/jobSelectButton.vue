<!--még nem jó -->

<template>
  <div id="jobButton">
    <b-container>
      <b-row>
        <b-con>
          <!-- Button trigger modal -->
          <button
            type="button"
            class="btn btn-primary btn-sm"
            data-toggle="modal"
            data-target="#modelId"
          >
            Launch
          </button>

          <!-- Modal -->
          <div
            class="modal fade"
            id="modelId"
            tabindex="-1"
            role="dialog"
            aria-labelledby="modelTitleId"
            aria-hidden="true"
          >
            <div class="modal-dialog" role="document">
              <div class="modal-content">
                <div class="modal-header">
                  <h5 class="modal-title">Modal title</h5>
                  <button
                    type="button"
                    class="close"
                    data-dismiss="modal"
                    aria-label="Close"
                  >
                    <span aria-hidden="true">&times;</span>
                  </button>
                </div>
                <div class="modal-body">Body</div>
                <div class="modal-footer">
                  <button
                    type="button"
                    class="btn btn-secondary"
                    data-dismiss="modal"
                  >
                    Close
                  </button>
                  <button type="button" class="btn btn-primary">Save</button>
                </div>
              </div>
            </div>
          </div>
        </b-con>
      </b-row>
    </b-container>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class jobSelect extends Vue {}
</script>

<style>
</style>