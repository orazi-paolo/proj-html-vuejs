<script>
// Import components
import ProfileCard from './ProfileCard.vue';

export default {
  data() {
    return {

    }
  },
  props: {
    userProfiles: {
      type: Array,
      required: true,
    }
  },
  components: {
    ProfileCard,
  }
}
</script>

<template>
  <div class="container">
    <div class="row">
      <div class="col" v-for="profile in userProfiles" :key="profile.id">
        <div class="card text-white p-3">
          <!-- Stars rate  -->
          <div class="stars-rate d-flex gap-1">
            <i class="bi bi-star-fill" v-for="i in profile.starsRate" :key="i"></i>
          </div>
          <!-- Description  -->
          <p class="mt-2">"{{ profile.description }}"</p>
          <ProfileCard :firstName="profile.firstName" :lastName="profile.lastName"
            :profileImgUrl="profile.profileImgUrl" :nationality="profile.nationality" />
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "/node_modules/bootstrap-icons/font/bootstrap-icons.css";

.card {
  background-color: #30405F;
  border-radius: 20px;
}

i.bi-star-fill {
  color: #F0C037;
}
</style>