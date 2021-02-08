<template >
  <div class="user-info-sec">
    <form class="user-info-form">
      <div class="input-group">
        <label
          class="input-label"
          for="name"
          @change="$emit('set-form-data', { name: 'event.target.value' })"
          >Name</label
        >
        <input name="name" type="text" placeholder="Inter Your Full Name" />
      </div>
      <div class="input-group">
        <label class="input-label" for="email" :v-model="email">Email</label>
        <input name="email" type="email" placeholder="Inter Your Email" />
      </div>
    </form>
  </div>
</template>
<script>
export default {
  name: "userInfoForm",
  data() {
    return {
      name: "",
      email: "",
    };
  },
};
</script>
<style lang="scss">
.user-info-sec {
  width: 80%;
  margin: auto;

  .user-info-form {
    padding-top: 31px;
    width: 85%;
    margin: auto;
    .input-group {
      margin-bottom: 22px;
      .input-label {
        display: inline-block;
        font-weight: 600;
        color: #848484;
        margin-bottom: 4px;
      }
      input {
        display: block;
        width: 100%;
        padding: 0.375rem 0.75rem;
        font-size: 1rem;
        line-height: 1.5;
        color: #495057;
        background-color: #fff;
        background-clip: padding-box;
        border: 1px solid #ced4da;
        border-radius: 0.25rem;
        transition: border-color 0.15s ease-in-out, box-shadow 0.15s ease-in-out;
        &::placeholder {
          font-size: 14px;
        }
      }
    }
  }
}
</style>