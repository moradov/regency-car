<template>
  <section class="features">
    <FeatureImage
      v-for="feat in features_data"
      :feature_image_url="feat.feat_img_url"
      :feature_text="feat.feat_text"
      :key="feat.feat_text"
    />
    text
  </section>
</template>
<script>
import FeatureImage from "./FeatureImage";

export default {
  components: { FeatureImage },
  data() {
    return {
      features_data: [
        {
          feat_img_url:
            "https://cdn2.buyacar.co.uk/sites/buyacar/files/volvo_s90_1.jpg",
          feat_text:
            "some bla bla hfgty rta  lorbs gdgsftz dgdvs dbbsnsbs sbshs gzd hdhzdh dzhzhdhzdhzhdh",
        },
        {
          feat_img_url:
            "https://cdn2.buyacar.co.uk/sites/buyacar/files/volvo_s90_1.jpg",
          feat_text:
            "some bla bla hfgty rta  lorbs gdgsftz dvs dbbsnsbs sbshs gzd hdhzdh dzhzhdhzdhzhdh",
        },
      ],
    };
  },
};
</script>
<style lang="scss">
.features {
  background-color: black;
  padding: 20px 0px;
}
</style>