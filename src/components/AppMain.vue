<script>
import AppMainFeatureMakeYourMark from './appMain-feature/AppMainFeatureMakeYourMark.vue'
import AppMainFeatureBattle from './appMain-feature/AppMainFeatureBattle.vue'
import AppMainFeatureFacts from './appMain-feature/AppMainFeatureFacts.vue'
import AppMainFeatureStreaming from './appMain-feature/AppMainFeatureStreaming.vue'
import AppMainFeatureFeedback from './appMain-feature/AppMainFeatureFeedback.vue'
import AppMainFeatureBanner from './appMain-feature/AppMainFeatureBanner.vue' 
import AppmainFeatureNews from './appMain-feature/AppmainFeatureNews.vue'; 



export default {
  data() {
    return {
      
    }
  },
  components: {
    AppMainFeatureMakeYourMark,
    AppMainFeatureBattle,
    AppMainFeatureFacts,
    AppMainFeatureStreaming,
    AppMainFeatureFeedback,
    AppMainFeatureBanner,
    AppmainFeatureNews,
  }
}
</script>

<template>

    <h1>
        Io sono AppMain
    </h1>
    <AppMainFeatureMakeYourMark />
    <AppMainFeatureBattle />
    <AppMainFeatureFacts />
    <AppMainFeatureStreaming />
    <AppMainFeatureFeedback />
    <AppMainFeatureBanner />
    <AppmainFeatureNews />



</template>

<style scoped>
</style>