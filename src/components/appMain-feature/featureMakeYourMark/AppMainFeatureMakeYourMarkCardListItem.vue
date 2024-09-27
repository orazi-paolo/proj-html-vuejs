<script>
export default {
  data() {
    return {

    }
  },
  props: {
    item: {
      type: Object,
      Required: true
    }
  },
  components: {

  },
  methods: {
    getImagePath(img) {
      return new URL(`../../../assets/icon/${img}`, import.meta.url).href
    }
  },
}
</script>

<!-- AppMainFeatureMakeYourMarkCardListItem -->
<template>
  <!-- li of the single card-gaming(item) -->
  <li class="card-gaming">
    <div class="box-icon">
      <!-- img of the icon of the single item -->
      <img :src="getImagePath(item.imgUrl)" :alt="item.imgUrl">
    </div>
    <div class="box-info">
      <!-- title of the single item -->
      <h3>{{ item.title }}</h3>
      <!-- description of the single item -->
      <p>{{ item.description }}</p>
    </div>
  </li>
</template>

<style lang="scss" scoped>
// Import stylesheet
@import "/src/style/utils.scss";

.card-gaming {
  display: flex;
  gap: 30px;


  .box-icon {
    flex-basis: 20%;
  }

  .box-info {
    flex-grow: 1;
    color: $white;

    h3,
    p {
      margin-bottom: $margin-lg;
    }
  }
}
</style>