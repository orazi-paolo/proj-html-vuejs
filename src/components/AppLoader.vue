<script>
export default {
  name: 'AppLoader',
};
</script>

<template>
  <div class="bg-loader d-flex justify-content-center align-items-center">
    <img src="../assets/preloader.gif" alt="Loader">
  </div>
</template>

<style lang="scss"scoped>
.bg-loader {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  background-color: #1c263d;
  z-index: 9999;
}
</style>