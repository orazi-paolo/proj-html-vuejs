<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import AppLoader from './components/AppLoader.vue';
import 'animate.css'
import WOW from 'wow.js'

new WOW().init()

export default {
  data() {
    return {
      loading: true
    }
  },
  components: {
    AppHeader,
    AppMain,
    AppFooter,
    AppLoader
  },
  mounted() {
    setTimeout(() => {
      this.loading = false;
    }, 2000)
  }
}
</script>

<template>
  <div v-if="loading">
    <AppLoader />
  </div>
  <div v-else>
    <AppHeader />
    <AppMain />
    <AppFooter />
  </div>

</template>

<style lang="scss">
@use "/node_modules/bootstrap/scss/bootstrap.scss";
@use "/src/style/general.scss";
@use '/node_modules/bootstrap-icons/font/bootstrap-icons.min.css';

.pointer {
  cursor: pointer;
}

/* width */
::-webkit-scrollbar {
  width: 10px;
}

/* Track */
::-webkit-scrollbar-track {
  background: #00013C;
}

/* Handle */
::-webkit-scrollbar-thumb {
  background: #5935C2;
}
</style>