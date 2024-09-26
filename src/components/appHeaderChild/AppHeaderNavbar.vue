<script>
import BaseButton from "../baseComponents/BaseButton.vue"
export default {
  data() {
    return {
      scroll: false,
    }
  },
  components: {
    BaseButton
  },
  methods: {
    isPageScrolled() {
      this.scroll = !this.scroll
    },

  },
  mounted() {
    window.addEventListener('scroll', this.isPageScrolled)
  }
}
</script>

<template>
  <nav class="navbar navbar-expand-lg" :class="{ 'nav-fixed': scroll } || { '': !scroll }">
    <div class="container">
      <a class="navbar-brand" href="#">
        <img src="../../assets/logo.png" alt="Logo Futio" class="d-inline-block align-text-top">
      </a>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav me-auto mb-2 mb-lg-0">
          <li class="nav-item">
            <a class="nav-link" aria-current="page" href="#">Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Link</a>
          </li>
          <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
              Dropdown
            </a>
          </li>
          <li class="nav-item">
            <a class="nav-link">Disabled</a>
          </li>
        </ul>
        <div class="d-flex">
          <BaseButton contentButton="LIVE STREAMING" :isArrow="false" />
        </div>
      </div>
    </div>
  </nav>
</template>

<style lang="scss" scoped>
a {
  color: white;
  font-family: "Orbitron", sans-serif;
}

.nav-fixed {
  background-color: #30405F;
  position: fixed;
  left: 0;
  right: 0;
  top: 0;
  z-index: 1;
}
</style>