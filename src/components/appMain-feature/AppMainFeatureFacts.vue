<script>
import FeatureFactsCardList from './featureFacts/FeatureFactsCardList.vue'
import FeatureFactsCardListItem from './featureFacts/FeatureFactsCardListItem.vue'
export default {
  data() {
    return {
      
    }
  },
  components: {
    FeatureFactsCardList,
    FeatureFactsCardListItem
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
      <FeatureFactsCardListItem />
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