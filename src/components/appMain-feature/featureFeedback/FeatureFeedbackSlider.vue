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
  },

  methods: {
    shuffleProfiles() {
      let middle = this.userProfiles[1]
      let first = this.userProfiles[0]
      // Change position of objects
      this.userProfiles[0] = middle
      this.userProfiles[1] = first

      // Rivert the user profiles array
      this.userProfiles.reverse()
    }
  },

  mounted() {
    setInterval(() => {
      this.shuffleProfiles()
    }, 2000)
  }
}
</script>

<template>
  <!-- Feedback Slider  -->
  <div class="container">
    <TransitionGroup class="row mt-5" name="scroll" tag="div">
      <div class="col" v-for="profile in userProfiles" :key="profile.id">
        <FeatureFeedbackSliderCard :firstName="profile.firstName" :lastName="profile.lastName"
          :nationality="profile.nationality" :description="profile.description" :profileImgUrl="profile.profileImgUrl"
          :starsRate="profile.starsRate" />
      </div>
    </TransitionGroup>
  </div>
</template>

<style lang="scss" scoped>
.scroll-move,
/* apply transition to moving elements */
.scroll-enter-active,
.scroll-leave-active {
  transition: all 0.5s ease;
}

.scroll-enter-from,
.scroll-leave-to {
  opacity: 0;
  transform: translateX(30px);
}

/* ensure leaving items are taken out of layout flow so that moving
   animations can be calculated correctly. */
.scroll-leave-active {
  position: absolute;
}
</style>