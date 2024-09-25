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
    BaseButton,
  }
}
</script>

<template>
<h1>
    Io sono AppHeader
</h1>
<AppHeaderNavbar />
<AppHeaderSection />
<BaseButton contentButton="PINCOPALLINO" :isArrow="true"/>


</template>

<style scoped>
</style>