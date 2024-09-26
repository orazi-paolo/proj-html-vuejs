<script>
// Import components
import BaseSectionTitle from '../baseComponents/BaseSectionTitle.vue';
export default {
  data() {
    return {
      // Variables
      offer: 70, // Store discount tot

    }
  },
  components: {
    BaseSectionTitle,
  }
}
</script>

<template>
  <!-- Banner section   -->
  <section class="bg-black p-5">
    <!-- Discount Title  -->
    <div
      class="container discount-title d-flex flex-column justify-content-center align-items-center text-white rounded-3 position-relative p-3  overflow-y-hidden">
      <h6>Make Offer</h6>
      <h1>Get {{ this.offer }}% Offer discount</h1>
      <!-- Phone img  -->
      <figure class="position-absolute w-25 start-0" id="phone">
        <img src="../../assets/banner-item-obj1.png" alt="phone banner">
      </figure>
      <!-- Headset img  -->
      <figure class="position-absolute w-25 end-0" id="headset">
        <img src="../../assets/banner-item-obj2.png" alt="phone banner">
      </figure>
      <button class="btn btn-secondary border-0 rounded-5 px-5 py-3 mt-3" id="btn">Get Offers</button>
    </div>
  </section>
</template>

<style lang="scss" scoped>
section {
  .discount-title {
    background-image: url("../../assets/banner-item-bg.png");
    background-size: cover;
    background-position: center;
    height: 300px;

  }

  #phone {
    top: 50px;

    img {
      max-width: 100%;
    }

  }

  #headset {
    bottom: 20px;

    img {
      max-width: 100%;
    }

  }

  #btn {
    font-size: 12px;
    background: rgba($color: black, $alpha: 0.3);
  }
}
</style>