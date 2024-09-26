<script>
import BaseSectionTitle from './../baseComponents/BaseSectionTitle.vue'
import AppMainFeatureMakeYourMarkCardList from './featureMakeYourMark/AppMainFeatureMakeYourMarkCardList.vue'

export default {
  data() {
    return {
      
    }
  },
  components:{
    BaseSectionTitle,
    AppMainFeatureMakeYourMarkCardList,

  }
}
</script>

<template>
  <!-- AppMainFeatureMakeYourMark -->
  <div class="container">
    <div class="row-battle">
      <div class="col-battle-left"></div>
      <div class="col-battle-right">
        <BaseSectionTitle 
          contentGreen="The Ultimate Competitive Gaming Platfrom" 
          mainTitle="Make Your Mark on the Battle Field"
          description="libero malesuada feugiat. Vivamus magna justo, lacinia eget consectetur sed, convallis at tellus. Cras ultricies ligula sed magna dictum porta."
        />
        <AppMainFeatureMakeYourMarkCardList />
      </div>
    </div>
  </div>
</template>

<style lang="scss">
  .row-battle{
    display: flex;
    justify-content: space-between;

    .col-battle-left{
    flex-basis: 40%;
    }
    .col-battle-right{
    flex-basis: 60%;
    }
  }
</style>