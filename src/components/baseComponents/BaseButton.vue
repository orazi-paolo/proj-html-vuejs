<script>
export default {
  data() {
    return {
    }
  },
  props: {
    contentButton: {
      required: true,
      type: String
    },
    isArrow: {
      type: Boolean,
      default: true,
      required: false
    }
  }
}
</script>

<template>
  <div id="base-button">
    <button class="fw-bold d-flex justify-content-center align-items-center">
      {{ contentButton }} <span v-if="isArrow"> <img class="img-color ps-2" src="/src/assets/svg/e-double-right-arrow.svg" alt="arrows-right"> </span>
    </button>
  </div>
</template>

<style lang="scss" scoped>
#base-button {
  display: inline-block;
  padding: 5px;
  border: 1px solid #08CB7B;
  border-radius: 30px;
  transition: border-color 0.3s;

  &:hover {
    border-color: #94CB53;

    button {
      background-color: #94CB53;
    }
  }


  button {
    border: none;
    border-radius: 30px;
    padding: 10px 15px;
    background-color: #08CB7B;
    transition: background-color 0.3s;
    .img-color{
      filter: invert(1);
    }
  }
}
</style>