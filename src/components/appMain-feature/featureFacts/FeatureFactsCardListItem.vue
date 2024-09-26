<script>
export default {
  data() {
    return {
      
    }
  },
  props:{
    fact:{
      required: true,
      type: Object,
    }
  }
}
</script>

<!-- FeatureFactsCardListItem -->
<template>
<li class="card-fact">
  {{ fact.title }}
</li>
</template>

<style lang="scss" scoped>

  .card-fact{
    flex-basis: calc(25% - 60px/4);
    text-align: center;
  }
</style>