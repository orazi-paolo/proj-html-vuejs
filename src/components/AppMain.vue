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
      scroll: false,
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
  },
  methods: {
    isPageScrolled() {
      this.scroll = true;
    },
  },
  mounted() {
    window.addEventListener('scroll', this.isPageScrolled)
  }
}
</script>

<template>
  <a href="#header-nav">
    <div class="to-top" :class="scroll ? 'active' : ''">
      <i class="bi bi-caret-up-square"></i>
    </div>
  </a>
  <AppMainFeatureMakeYourMark />
  <AppMainFeatureBattle />
  <AppMainFeatureFacts />
  <AppMainFeatureStreaming />
  <AppMainFeatureFeedback />
  <AppMainFeatureBanner />
  <AppmainFeatureNews />
</template>

<style scoped>
.to-top {
  position: fixed;
  bottom: 0;
  right: 30px;
  width: 50px;
  height: 50px;
  background-color: #94CB53;
  display: flex;
  font-size: 30px;
  color: white;
  justify-content: center;
  align-items: center;
  border-radius: 5px;
  z-index: 3;
  transition: 1s;
  transform: translateY(100%);
}

.to-top.active {
  transform: translateY(-90%);
}
</style>