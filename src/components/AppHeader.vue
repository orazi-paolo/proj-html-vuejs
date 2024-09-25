<script>
import AppHeaderNavbar from './appHeaderChild/AppHeaderNavbar.vue'
import AppHeaderSection from './appHeaderChild/AppHeaderSection.vue'
export default {
  data() {
    return {
      
    }
  },
  components: {
    AppHeaderNavbar,
    AppHeaderSection
  }
}
</script>

<template>
<h1>
    Io sono AppHeader
</h1>
<AppHeaderNavbar />
<AppHeaderSection />

</template>

<style scoped>
</style>