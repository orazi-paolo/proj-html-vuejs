<script>
import AppFooterNewsLetter from './appFooterChild/AppFooterNewsLetter.vue'
import AppFooterColList from './appFooterChild/AppFooterColList.vue'
export default {
  data() {
    return {
      
    }
  },
  components: {
    AppFooterNewsLetter,
    AppFooterColList
  }
}
</script>

<template>
  <footer>
    <AppFooterNewsLetter />
    <AppFooterColList />

  </footer>

</template>

<style lang="scss" scoped>
</style>