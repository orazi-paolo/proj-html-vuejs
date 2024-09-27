<script>
// Import components
import ProfileCard from './ProfileCard.vue';

export default {
  data() {
    return {

    }
  },
  props: {
    firstName: {
      type: String,
      required: true,
    },
    lastName: {
      type: String,
      required: true,
    },
    nationality: {
      type: String,
      required: true,
    },
    profileImgUrl: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
    starsRate: {
      type: Number,
      required: true,
    },
  },
  components: {
    ProfileCard,
  }
}
</script>

<template>
  <!-- FeedBack Card -->
  <div class="card text-white p-3">
    <!-- Stars rate  -->
    <div class="stars-rate d-flex gap-1">
      <i class="bi bi-star-fill" v-for="i in starsRate" :key="i"></i>
    </div>
    <!-- Description  -->
    <p class="mt-2">"{{ description }}"</p>
    <ProfileCard :firstName="firstName" :lastName="lastName" :profileImgUrl="profileImgUrl"
      :nationality="nationality" />
  </div>
</template>

<style lang="scss" scoped>
// Import stylesheet
@import "/src/style/utils.scss";

.card {
  background-color: $cardsBg;
  border-radius: $lg;
}

i.bi-star-fill {
  color: $rateStar;
}
</style>