<script>
import FeatureFactsCardList from './featureFacts/FeatureFactsCardList.vue'
export default {
  data() {
    return {

    }
  },
  components: {
    FeatureFactsCardList
  }
}
</script>

<!-- AppMainFeatureFacts -->
<template>
  <section class="facts-background">
    <div class="container wow animate__animated animate__fadeInUp" data-wow-duration="1s">
      <h3 class="title-section">
        Futio Quick Facts
      </h3>
      <FeatureFactsCardList />
    </div>
  </section>
</template>

<style lang="scss" scoped>
// Import stylesheet
@import "/src/style/utils.scss";

.facts-background {
  background-color: $black;
  padding: 100px;

  .title-section {
    color: $white;
    font-size: 50px;
    text-align: center;
  }
}
</style>