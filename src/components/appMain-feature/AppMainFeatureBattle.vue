<script>
import AppMainFeatureBattleCardList from './featureBattle/FeatureBattleCardList.vue'
import BaseSectionTitle from './../baseComponents/BaseSectionTitle.vue'
import BaseButton from './../baseComponents/BaseButton.vue'

export default {
  data() {
    return {
      
    }
  },
  components: {
    BaseSectionTitle,
    AppMainFeatureBattleCardList,
    BaseButton,
  }
}
</script>

<!-- FeatureBattle -->
<template>
  <section class="battle-background">
          <BaseSectionTitle 
            contentGreen="Trending Battle"
            mainTitle="Keep Eyes & Manage upcoming Battle"
            description="libero malesuada feugiat. Vivamus magna justo, lacinia eget consectetur sed, convallis at tellus. Cras ultricies ligula sed magna dictum porta."
            :isCenter='true'
          />
      <AppMainFeatureBattleCardList /> 
      <div class="text-center">
        <!-- button imported from BaseComponents -->
        <BaseButton contentButton="VIEW ALL MATCH"/>
      </div>
  </section>
</template>

<style lang="scss" scoped>

.battle-background{
  background-color: #212833;
  padding: 100px 0;
}

</style>