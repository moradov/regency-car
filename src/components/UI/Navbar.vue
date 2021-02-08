<template>
  <nav class="nav">
    <ul class="left-content u-list">
      <li class="li-item">Regency Cars</li>
    </ul>
    <ul class="right-content u-list">
      <li class="li-item">About</li>
      <li class="li-item">Booking</li>
      <li class="li-item">Contact ass</li>
    </ul>
  </nav>
</template>
<script>
// import test from '../../assets/sass/_mixins' ;
export default {
  name: "Navbar",
  props: ["logo", "navItems"],
};
</script>

<style lang="scss">
.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: black;
  color: #fff;
  padding: 10px 40px;
  .left-content,
  .right-content {
    margin: 0;
    padding: 0;
    list-style: none;
  }
  .right-content {
    display: flex;
    li {
      padding: 10px;
    }
  }
}
</style>
