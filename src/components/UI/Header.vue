<template>
  <header class="header">
    <!-- <div class="header-wrapper"></div> -->
    <div class="header-content">
      <h2>Its time to meet Your Dream Car</h2>
      <p>
        with this pandamic crisis you don't need came to our agency , you can
        Book from here
      </p>
      <button class="booking">Booking</button>
    </div>
  </header>
</template>
<script>
export default {
  name: "Header",
};
</script>
<style lang='scss' >
.header {
  height: 100vh;
  position: relative;
  background-image: url("https://cdn2.buyacar.co.uk/sites/buyacar/files/volvo_s90_1.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  .header-wrapper {
    width: 100%;
    height: 100%;
    position: absolute;
  }
  .header-content {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 100%;
    background-color: #ff00004d;

    button {
      font-size: 18px;
      padding: 8px 21px;
      border-radius: 5px;
      border: none;
      cursor: pointer;
      color: #fff;
      background-color: red;
    }
  }
}
</style>