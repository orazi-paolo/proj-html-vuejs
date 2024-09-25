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

<template>
  <h3>
    feature facts
  </h3>
  <FeatureFactsCardList />
  <FeatureFactsCardListItem />
</template>

<style scoped>
</style>