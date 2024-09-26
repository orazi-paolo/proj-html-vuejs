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
  <ul id="list-facts">
    <FeatureFactsCardListItem 
      v-for="(fact, index) in listFacts" :key="index" :fact="fact"
    />
  </ul>
</template>

<style lang="scss">
  #list-facts{
    width: 100%;
    list-style-type: none;
    display: flex;
    gap: 20px;
    margin-top: 50px;
  }
</style>