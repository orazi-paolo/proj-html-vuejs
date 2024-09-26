<script>
import AppMainFeatureBattleCardList from './featureBattle/FeatureBattleCardList.vue'
import AppMainFeatureBattleCardListItem from './featureBattle/BattleCardListItem.vue'
import BaseSectionTitle from './../baseComponents/BaseSectionTitle.vue'
export default {
  data() {
    return {
      
    }
  },
  components: {
    BaseSectionTitle,
    AppMainFeatureBattleCardList,
    AppMainFeatureBattleCardListItem,
  }
}
</script>

<template>
  <div class="background">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-6">
          <BaseSectionTitle 
            contentGreen="Trending Battle"
            mainTitle="Keep Eyes & Manage upcoming Battle"
            description="libero malesuada feugiat. Vivamus magna justo, lacinia eget consectetur sed, convallis at tellus. Cras ultricies ligula sed magna dictum porta."
            :isCenter=true
          />
        </div>
      </div>
      <AppMainFeatureBattleCardList />
      <AppMainFeatureBattleCardListItem />
      
    </div>
  </div>
</template>

<style lang="scss">

</style>