<template>
  <div class="app">
    <input type="text" v-model="inputValue" />
    <p>{{ "the interd value is " + inputValue }}</p>
  </div>
</template>
<script>
export default {
  name: "Test",
  data() {
    return { inputValue: "" };
  },
};
</script>