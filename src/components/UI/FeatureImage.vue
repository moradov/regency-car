<template>
  <div class="feat-sec">
    <div class="feat-img-sec">
      <img :src="feature_image_url" />
    </div>
    <div class="feat-text-sec">
      <p>{{ feature_text }}</p>
    </div>
  </div>
</template>
<script>
export default {
  name: "FeatureImage",
  props: ["feature_image_url", "feature_text"],
};
</script>
<style lang="scss">
.feat-sec {
  width: 70%;
  margin: 10px auto;
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(367px, 1fr));
  grid-auto-rows: 302px;

  @media (max-width: 500px) {
    flex-direction: column;
  }
  .feat-img-sec {
    img {
      width: 100%;
      height: 100%;
    }
  }
  .feat-text-sec {
    background-color: #fff;
    padding: 25px;
    p {
      color: rgb(97, 97, 97);
    }
  }
}
</style>