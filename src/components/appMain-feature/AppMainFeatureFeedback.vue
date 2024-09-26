<script>
// Import components
import FeatureFeedbackSlider from './featureFeedback/FeatureFeedbackSlider.vue'
import BaseSectionTitle from '../baseComponents/BaseSectionTitle.vue'

export default {
  data() {
    return {

    }
  },
  components: {
    FeatureFeedbackSlider,
    BaseSectionTitle,
  }
}
</script>

<template>
  <!-- Feedback Section  -->
  <section class="bg-black p-5">
    <div class="container w-75">
      <BaseSectionTitle contentGreen="Futio Feedback" mainTitle="What Our Gamers Say" description="libero malesuada feugiat. Vivamus magna justo, lacinia eget consectetur sed, convallis at tellus.
        Cras ultricies ligula sed magna dictum porta." isCenter />
      <FeatureFeedbackSlider />
    </div>
  </section>
</template>

<style lang="scss" scoped></style>