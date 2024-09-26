<script>
import BaseSectionTitle from './../baseComponents/BaseSectionTitle.vue'
import AppMainFeatureMakeYourMarkCardList from './featureMakeYourMark/AppMainFeatureMakeYourMarkCardList.vue'
import BaseButton from './../baseComponents/BaseButton.vue'

export default {
  data() {
    return {
      imgUrl: 'features-illus.png'
    }
  },
  components:{
    BaseSectionTitle,
    AppMainFeatureMakeYourMarkCardList,
    BaseButton,
  }
}
</script>

<!-- AppMainFeatureMakeYourMark -->
<template>
  <section class="makeYourMark-background">
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
          <BaseButton contentButton="PLAN NOW"/>
        </div>
      </div>
    </div>
    <!-- main img in position absolute -->
    <img class="img-gamer" :src="`../..//src/assets/${imgUrl}`" :alt="imgUrl">
  </section>
</template>

<style lang="scss">
  .makeYourMark-background{
    background-color: #000;
    padding: 100px 0;
    position: relative;
    .row-battle{
      display: flex;
      justify-content: space-between;

      .col-battle-left{
      flex-basis: 40%;
      }
      .col-battle-right{
      flex-basis: 50%;
      }
    }
    img.img-gamer{
      height: 700px;
      position: absolute;
      top: 12%;
      left: -12%;
    }
  }
</style>