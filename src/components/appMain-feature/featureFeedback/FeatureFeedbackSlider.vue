<script>
// Import components
import FeatureFeedbackSliderCard from './FeatureFeedbackSliderCard.vue';
export default {
  data() {
    return {
      //Variables
      userProfiles: [
        {
          id: 3,
          firstName: "Kim",
          lastName: "Ramos",
          nationality: "Serbia",
          profileImgUrl: "testimonials-image-3.png",
          description: "Lorem losum dolor sit amet, Collseolelur daloisone elit, Se do eiusmod tempor.",
          starsRate: 5
        },
        {
          id: 2,
          firstName: "Garry",
          lastName: "Francis",
          nationality: "Kiribati",
          profileImgUrl: "testimonials-image-2.png",
          description: "Lorem losum dolor sit amet, Collseolelur daloisone elit, Se do eiusmod tempor.",
          starsRate: 5
        },
        {
          id: 1,
          firstName: "Merle",
          lastName: "Fisher",
          nationality: "United States",
          profileImgUrl: "testimonials-image-1.png",
          description: "Lorem losum dolor sit amet, Collseolelur daloisone elit, Se do eiusmod tempor.",
          starsRate: 5
        },
      ]

    }
  },
  components: {
    FeatureFeedbackSliderCard,
  }
}
</script>

<template>
  <!-- Feedback Slider  -->
  <div class="container">
    <div class="row mt-5">
      <div class="col" v-for="profile in userProfiles" :key="profile.id">
        <FeatureFeedbackSliderCard :firstName="profile.firstName" :lastName="profile.lastName"
          :nationality="profile.nationality" :description="profile.description" :profileImgUrl="profile.profileImgUrl"
          :starsRate="profile.starsRate" />
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped></style>