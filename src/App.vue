<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import 'animate.css'
import WOW from 'wow.js'

new WOW().init()

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
@use '/node_modules/bootstrap-icons/font/bootstrap-icons.min.css';
.pointer{
  cursor: pointer;
}
</style>