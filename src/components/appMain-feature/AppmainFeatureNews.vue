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
      <!-- I create a container to add margins and padding to the sides -->
      <div class="container">
        <!-- I use a base component that was previously pre-configured -->
        <BaseSectionTitle isCenter contentGreen="Latest News" mainTitle="Stay Updated With Our Latest News Articles" description="libero malesuada feugiat. Vivamus magna justo, lacinia eget consectetur sed, convailis at tellus. Cras ultricies ligula sed magna dictum porta." />
      </div>
      <!-- I organize the cards in another component -->
      <FeatureNewsList />
    </section>

</template>

<style lang="scss" scoped>
//Background color of the section
  .base-background{
    background-color: black;
  }
</style>