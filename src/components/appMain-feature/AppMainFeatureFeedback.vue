<script>
import FeatureFeedbackSlider from './featureFeedback/FeatureFeedbackSlider.vue'
import FeatureFeedbackSliderCard from './featureFeedback/FeatureFeedbackSliderCard.vue'
export default {
  data() {
    return {
      
    }
  },
  components: {
    FeatureFeedbackSlider,
    FeatureFeedbackSliderCard

  }
}
</script>

<template>
  <h3>
    feature feedback
  </h3>
  <FeatureFeedbackSlider />
  <FeatureFeedbackSliderCard />
</template>

<style scoped>
</style>