<script>
export default {
  //  take the props sent by the parent
  props: {
    image:{
      type: String,
      required: true
    },
    title:{
      type: String,
      required: true
    },
    clock:{
      type: String,
      required: true
    },
    visual:{
      type: String,
      required: true
    },
    date: {
      type: String,
      required: true
    }
  }
}
</script>

<template>
  <!-- compose the cards using the props received from the parent -->
        <div class="card bg-dark text-white mb-4 d-flex flex-row">
            <img class="img-card-news pointer" :src="image" :alt="title">
            <div class="card-body">
              <div class="metadata">
                <span class="pe-3"><span><img class="pe-1" src="../../../assets/icon/clock.png" alt="icon clock"></span>{{ clock }}</span>
                <span class="pe-3"><span><img class="pe-1" src="../../../assets/icon/eye.png" alt="icon eye"></span>{{ visual }}</span>
                <span class="pe-3"><span><img class="pe-1" src="../../../assets/icon/calendar.png" alt="icon calendar"></span>{{ date }}</span>
              </div>
              <h5 class="card-title mt-2 pointer">{{ title }}</h5>
            </div>
        </div>
</template>

<style lang="scss" scoped>
.card{
  border-radius: 20px;
  background-color: #30405F !important;
  .metadata{
    color: #94CB53;
    font-size: 11px;
  }
}
.img-card-news{
  border-radius: 20px 0 0 20px;
  max-width: 100%;
  height: calc(500px / 3);
}
</style>