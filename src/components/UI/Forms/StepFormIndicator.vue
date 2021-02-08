<template>
  <div class="steps-monitor">
    <ul class="steps-list">
      <li
        v-for="step in steps"
        :class="{
          'step-item ': true,
          valid: current_step > step.step_index,
        }"
        :key="step.step_index"
      >
        {{ current_step > step.step_index ? "Valid" : step.step_index }}
      </li>
      <li class="center-line"></li>
    </ul>
  </div>
</template>
<script>
export default {
  name: "BookingForm",
  props: ["steps", "current_step"],
  data() {
    return {};
  },
  created() {
    console.log(this.current_step);
  },
};
</script>
<style lang="scss">
.steps-monitor {
  width: 80%;
  margin: auto;
  ul {
    list-style: none;
    display: flex;
    position: relative;
    justify-content: space-between;
    .step-item {
      font-size: 23px;
      background-color: red;
      border-radius: 71%;
      width: 70px;
      height: 70px;
      text-align: center;
      display: flex;
      justify-content: center;
      align-items: center;
      z-index: 9999;
      color: #fff;
    }
    .valid {
      background-color: rgb(54, 204, 54);
      color: #fff;
    }
    .center-line {
      position: absolute;
      width: 100%;
      height: 3px;
      background-color: black;
      top: 33px;
    }
  }
}
</style>
