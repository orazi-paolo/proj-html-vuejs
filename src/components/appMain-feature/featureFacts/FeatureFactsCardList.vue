<script>
import FeatureFactsCardListItem from './FeatureFactsCardListItem.vue'

export default {
  data() {
    return {
      listFacts:[
        {
          title:'Twitch Streams',
          min: 0,
          max: 5500,
        },
        {
          title:'Total Games',
          min: 0,
          max: 800,
        },
        {
          title:'Youtube Streams',
          min: 0,
          max: 5500,
        },
        {
          title:'Pro Team',
          min: 0,
          max: 500,
        }
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
    <!-- sended by props to FeatureFactsCardListItem the items(fact) of listFacts[] with v-for-->
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