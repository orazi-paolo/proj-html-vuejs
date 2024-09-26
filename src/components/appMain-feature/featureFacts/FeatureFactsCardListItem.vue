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
  <h5>numb</h5>
  <p>{{ fact.title }}</p>
</li>
</template>

<style lang="scss" scoped>

  .card-fact{
    flex-basis: calc(25% - 60px/4);
    text-align: center;
    border: 1px solid #10161F;
    border-radius: 50px;
    overflow: hidden;
    padding: 50px 0;

    h5{
      color: #fff;
      margin-bottom: 20px;
      font-size: 50px;
      font-weight: 600;
    }

    p{
      color: #94CB53;
    }
  }
</style>