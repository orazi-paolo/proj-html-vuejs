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
    <div class="container">
      <h3 class="title-section">
        Futio Quick Facts
      </h3>
      <FeatureFactsCardList />
    </div>
  </section>
</template>

<style lang="scss" scoped>

.facts-background{
  background-color: #000;
  padding: 100px;

  .title-section{
    color: #fff;
    font-size: 50px;
    text-align: center;
  }
}
</style>