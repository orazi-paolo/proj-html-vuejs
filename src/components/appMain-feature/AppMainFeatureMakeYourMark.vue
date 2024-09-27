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
  components: {
    BaseSectionTitle,
    AppMainFeatureMakeYourMarkCardList,
    BaseButton,
  }
}
</script>

<!-- AppMainFeatureMakeYourMark -->
<template>
  <section class="makeYourMark-background">
    <div class="container wow animate__animated animate__fadeInUp" data-wow-duration="1s">
      <div class="row-battle">
        <div class="col-battle-left"></div>
        <div class="col-battle-right">
          <BaseSectionTitle contentGreen="The Ultimate Competitive Gaming Platfrom"
            mainTitle="Make Your Mark on the Battle Field"
            description="libero malesuada feugiat. Vivamus magna justo, lacinia eget consectetur sed, convallis at tellus. Cras ultricies ligula sed magna dictum porta." />
          <AppMainFeatureMakeYourMarkCardList />
          <BaseButton contentButton="PLAN NOW" />
        </div>
      </div>
    </div>
    <!-- main img in position absolute -->
    <img class="img-gamer" :src="`../..//src/assets/${imgUrl}`" :alt="imgUrl">
  </section>
</template>

<style lang="scss">
// Import stylesheet
@import "/src/style/utils.scss";

.makeYourMark-background {
  background-color: $black;
  padding: 100px 0;
  position: relative;

  .row-battle {
    display: flex;
    justify-content: space-between;

    .col-battle-left {
      flex-basis: 40%;
    }

    .col-battle-right {
      flex-basis: 50%;
    }
  }

  img.img-gamer {
    height: 600px;
    position: absolute;
    top: 12%;
    left: -200px;
    @media (max-width: 1150px){
      position: static;
      top: auto;
      left: auto;
      display: block;
      margin-top: 50px;
    }
    @media (min-width: 1400px){
      left: -100px;
    }
    @media (min-width: 1700px){
      left: 100px;
    }
  }
}
</style>