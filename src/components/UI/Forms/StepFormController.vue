<template>
  <div class="f-control">
    <button
      class="btn prev"
      v-if="current_step > 1"
      @click="$emit('prev-clicked')"
    >
      Prev
    </button>
    <button
      class="btn next"
      v-if="current_step !== 4"
      @click="$emit('next-clicked')"
    >
      Next
    </button>
  </div>
</template>
<script>
export default {
  name: "StepFormController",
  props: ["current_step", "steps_max_index"],
};
</script>
<style lang="scss">
.f-control {
  display: flex;
  justify-content: center;
  .btn {
    font-size: 18px;
    padding: 8px 21px;
    border-radius: 5px;
    border: none;
    cursor: pointer;
    color: #fff;
    background-color: #284ac6;
    margin-left: 13px;
  }
}
</style>