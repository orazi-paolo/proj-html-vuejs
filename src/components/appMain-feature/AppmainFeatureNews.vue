<script>
import FeatureNewsList from './featureNews/FeatureNewsList.vue'
import BaseSectionTitle from '../baseComponents/BaseSectionTitle.vue'
export default {
  data() {
    return {

    }
  },
  components: {
    FeatureNewsList,
    BaseSectionTitle
  }
}
</script>

<template>
  <section class="base-background pt-5">
    <!-- create a container to add margins and padding to the sides -->
    <div class="container">
      <!-- I use a base component that was previously pre-configured -->
      <BaseSectionTitle isCenter contentGreen="Latest News" mainTitle="Stay Updated With Our Latest News Articles"
        description="libero malesuada feugiat. Vivamus magna justo, lacinia eget consectetur sed, convailis at tellus. Cras ultricies ligula sed magna dictum porta."
        class="wow animate__animated animate__fadeInUp" data-wow-duration="1s" />
    </div>
    <!-- organize the cards in another component -->
    <FeatureNewsList class="wow animate__animated animate__fadeInUp" data-wow-duration="1s" />
  </section>

</template>

<style lang="scss" scoped>
// Import stylesheet
@import "/src/style/utils.scss";

//Background color of the section
.base-background {
  background-color: $black;
  padding-bottom: 200px;
}
</style>