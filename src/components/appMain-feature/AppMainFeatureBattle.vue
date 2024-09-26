<script>
import AppMainFeatureBattleCardList from './featureBattle/FeatureBattleCardList.vue'
import AppMainFeatureBattleCardListItem from './featureBattle/BattleCardListItem.vue'
export default {
  data() {
    return {
      
    }
  },
  components: {
    AppMainFeatureBattleCardList,
    AppMainFeatureBattleCardListItem

  }
}
</script>

<template>
  <h3>
    feature battle
  </h3>
  <AppMainFeatureBattleCardList />
  <AppMainFeatureBattleCardListItem />
</template>

<style scoped>
</style>