<script>
export default {
  data() {
    return {
      
    }
  },
  props: {
    title: {
      type: String,
      required: true
    },
    items: {
      type: Array,
      required: true
    }
  }
}
</script>

<template>
  <div class="col-2">
    <h5>
      {{ title }}
    </h5>
    <ul>
      <li v-for="item in items" :key="item"> {{ item }}</li>
    </ul>
  </div>
</template>

<style scoped>
</style>