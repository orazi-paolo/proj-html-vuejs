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
  <div class="container">
    <div class="row-battle">
      <div class="col-battle-left"></div>
      <div class="col-battle-right">
        <AppMainFeatureBattleCardList />
        <AppMainFeatureBattleCardListItem />
      </div>
    </div>
  </div>
 
</template>

<style lang="scss">
  .row-battle{
    display: flex;

  .col-battle-left{
  flex-basis: 40%;
  }
  .col-battle-rifght{
  flex-basis: 60%;
  }
  }
</style>