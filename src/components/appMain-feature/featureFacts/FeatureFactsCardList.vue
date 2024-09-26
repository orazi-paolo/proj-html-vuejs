<script>
import FeatureFactsCardListItem from './FeatureFactsCardListItem.vue'

export default {
  data() {
    return {
      listFacts:[
        {title:'Twitch Streams'},
        {title:'Total Games'},
        {title:'Youtube Streams'},
        {title:'Pro Team'}
      ]
    }
  },
  components: {
    FeatureFactsCardListItem
  }
}
</script>

<!-- FeatureFactsCardList -->
<template>
  <ul>
    <FeatureFactsCardListItem />
  </ul>
</template>

<style scoped>
</style>