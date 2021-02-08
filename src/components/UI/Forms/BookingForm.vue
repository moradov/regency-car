<template>
  <div class="booking-form">
    <StepFormIndicator :steps="steps" :current_step="current_step" />
    <UserInfoForm v-if="current_step === 1" @set-form-data="setForm" />

    <div v-else-if="this.current_step == 2">booking detail</div>
    <div v-else-if="this.current_step == 3">final steps</div>
    <StepFormController
      :current_step="current_step"
      :steps_max_index="steps.length"
      @next-clicked="nextFunc"
      @prev-clicked="prevFunc"
    />
  </div>
</template>
<script>
import StepFormIndicator from "./StepFormIndicator";
import UserInfoForm from "./UserInfoForm";
import StepFormController from "./StepFormController";
export default {
  components: { StepFormIndicator, UserInfoForm, StepFormController },
  name: "BookingForm",
  data() {
    return {
      current_step: 1,
      form_data: {
        name: "",
        email: "",
        car: "",
        booking_date: "",
      },

      steps: [
        { step_index: 1, step_content: 1 },
        { step_index: 2, step_content: 2 },
        { step_index: 3, step_content: 3 },
      ],
    };
  },
  methods: {
    nextFunc() {
      this.current_step = this.current_step + 1;

      console.log(this.current_step);
      // if (this.current_step != this.steps.length) {
      //   this.current_step = this.current_step + 1;

      //   console.log("next");
      //   console.log(this.current_step);
      // } else {
      //   console.log(this.current_step);
      //   console.log("stop");
      // }
    },
    prevFunc() {
      this.current_step = this.current_step - 1;
      console.log(this.current_step);
      // if (!this.current_step == 1) {
      //   this.current_step = this.current_step - 1;
      //   console.log(this.current_step);
      //   console.log("next");
      // } else {
      //   console.log("stop");
      //   console.log(this.current_step);
      // }
    },
    setForm(data) {
      console.log(data);
      // this.form_data = {
      //   ...this.form_data,
      //   ...data,
      // };
    },
  },
};
</script>
<style lang="scss">
.booking-form {
  height: 600px;
  margin-top: 50px;
}
</style>
