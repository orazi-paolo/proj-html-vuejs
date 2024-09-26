<script>
import AppHeaderNavbar from './appHeaderChild/AppHeaderNavbar.vue'
import AppHeaderSection from './appHeaderChild/AppHeaderSection.vue'
import BaseButton from './baseComponents/BaseButton.vue'
export default {
  data() {
    return {

    }
  },
  components: {
    AppHeaderNavbar,
    AppHeaderSection,
    BaseButton
  }
}
</script>

<template>
  <header>
    <AppHeaderNavbar />
    <AppHeaderSection />
  </header>
</template>

<style scoped>
header {
  height: 900px;
  background-image: url(../assets/index-banner-bg.png);
  background-size: cover;
}
</style>