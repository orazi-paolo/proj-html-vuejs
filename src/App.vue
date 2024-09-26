<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
export default {
  data() {
    return {
      
    }
  },
  components: {
    AppHeader,
    AppMain,
    AppFooter
  }
}
</script>

<template>

  <AppHeader />
  <AppMain />
  <AppFooter />

</template>

<style lang="scss">
@use "/node_modules/bootstrap/scss/bootstrap.scss";
@use "/src/style/general.scss";
@use '/node_modules/bootstrap-icons/font/bootstrap-icons.min.css'
</style>