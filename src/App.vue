<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import AppLoader from './components/AppLoader.vue';
import 'animate.css';
import WOW from 'wow.js';

new WOW().init();

export default {
  data() {
    return {
      loading: true,
    };
  },
  components: {
    AppHeader,
    AppMain,
    AppFooter,
    AppLoader,
  },
  mounted() {
    // simulates the loading
    setTimeout(() => {
      this.loading = false;
    }, 1000);
  },
};
</script>

<template>
  <div>
    <!-- Loader with transition -->
    <transition name="fade-disperse">
      <AppLoader v-if="loading" />
    </transition>

    <div class="main-content">
      <AppHeader />
      <AppMain />
      <AppFooter />
    </div>
  </div>
</template>

<style lang="scss">
// Import from libraries
@use "/node_modules/bootstrap/scss/bootstrap.scss";
@use '/node_modules/bootstrap-icons/font/bootstrap-icons.min.css';
// Import stylesheet
@use "/src/style/general.scss";
@import "./style/utils.scss";


.fade-disperse-enter-active,
.fade-disperse-leave-active .fade-disperse-enter-active,
.fade-disperse-leave-active {
  transition: all 1s ease;
}


.fade-disperse-leave-to {
  opacity: 0;
  transform: scale(1.1);
  filter: blur($sm);
}

.main-content {
  position: relative;
  z-index: 2;
}


.AppLoader {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: rgba($white, 0.9);
  z-index: 3;
}

.pointer {
  cursor: pointer;
}

/* width */
::-webkit-scrollbar {
  width: $md;
}

/* Track */
::-webkit-scrollbar-track {
  background: $trackBg;
}

/* Handle */
::-webkit-scrollbar-thumb {
  background: $scrollBarThumbBg;
}
</style>