<template>
  <section class='hl_page-creator--section'>
    <div class="hl_page-creator--actions">
      <div class="move-actions">
        <span data-tooltip="tooltip" data-placement="right" title="Up"><i class="icon icon-arrow-up-2"></i></span>
        <span data-tooltip="tooltip" data-placement="right" title="Down"><i
          class="icon icon-arrow-down-2"></i></span>
      </div>
      <div class="more-actions">
        <span data-tooltip="tooltip" data-placement="left" title="Settings"><i class="fas fa-cog"></i></span>
        <span data-tooltip="tooltip" data-placement="left" title="Clone"><i class="far fa-eye"></i></span>
        <span data-tooltip="tooltip" data-placement="left" title="Save"><i class="far fa-copy"></i></span>
        <span data-tooltip="tooltip" data-placement="left" title="Delete" @click="$emit('delete-section', index)"><i class="far fa-trash-alt"></i></span>
      </div>
    </div>
    <span class="add-new-section" @click="$emit('add-section')" data-tooltip="tooltip" data-placement="bottom" title="Add New Section"><i class="icon icon-plus"></i></span>
    <div href="#" class="new-row-blank">
      <span class="btn btn-light5 btn-slim" @click="addRow">Add New Row</span>
    </div>
  </section>
</template>

<script>
  export default {
    props: ['index'],
    methods() {

    }
  }
</script>

<style>
  .hl_page-creator--section{
    margin-bottom: 14px;
  }
  .hl_page-creator--section:hover {
    border-color: #37ca37;
  }
  .hl_page-creator--section:hover .hl_page-creator--actions, .hl_page-creator--section:hover .add-new-section {
    opacity: 1
  }
</style>