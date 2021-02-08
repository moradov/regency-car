<template>
  <div>
    <Navbar
      :logo="'<div> my logo </div>'"
      :navItems="['About', 'Booking', 'Contact']"
    />
    <Header />
    <Features />
    <BookingForm />
  </div>
</template>

<script>
import Navbar from "./components/UI/Navbar";
import Header from "./components/UI/Header";
import Features from "./components/UI/Features";
import BookingForm from "./components/UI/Forms/BookingForm";
export default {
  name: "App",
  components: { Navbar, Header, Features, BookingForm },
  data() {
    return {
      msg: "hello",
      arabVal: null,
      usaVal: null,
    };
  },

  methods: {
    formSubmit() {
      this.inptVal = null;
    },
  },
};
</script>
<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: sans-serif;
}
</style>
