<script>
import FeatureNewsList from './featureNews/FeatureNewsList.vue'
import FeatureNewsListCard from './featureNews/FeatureNewsListCard.vue'
export default {
  data() {
    return {

    }
  },
  components: {
    FeatureNewsList,
    FeatureNewsListCard

  }
}
</script>

<template>
    <h3>
        feature news
    </h3>
    <FeatureNewsList />
    <FeatureNewsListCard />

</template>

<style scoped>
</style>