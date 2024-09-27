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
      {{ contentButton }} <span v-if="isArrow"> <img class="img-color ps-2"
          src="/src/assets/svg/e-double-right-arrow.svg" alt="arrows-right"> </span>
    </button>
  </div>
</template>

<style lang="scss" scoped>
// Import stylesheet
@import "/src/style/utils.scss";

#base-button {
  display: inline-block;
  padding: $padding-sm;
  border: 1px solid $brightTeal;
  border-radius: $xlg;
  transition: border-color 0.3s;

  &:hover {
    border-color: $lightOliveGreen;

    button {
      background-color: $lightOliveGreen;
    }
  }


  button {
    border: none;
    border-radius: $xlg;
    padding: $padding-md 15px;
    background-color: $brightTeal;
    transition: background-color 0.3s;

    .img-color {
      filter: invert(1);
    }
  }
}
</style>