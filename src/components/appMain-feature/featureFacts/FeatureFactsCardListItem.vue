<script>
export default {
  data() {
    return {
      incrementedNumber: 0,
    }
  },
  props:{
    fact:{
      required: true,
      type: Object,
    }
  },
  methods:{
    // function that generates a random number from min to max
    getRandomNumber(min, max){
      // generate the random number
      let result = Math.floor(Math.random() * (max + 1 -min)) + min;
      return result;
    },

    getIncreaseNumber(){
      // call getRandomNumber
      this.incrementedNumber = this.getRandomNumber(this.fact.min, this.fact.max);

      // start incrementing the number every 25ms
      const increaseNumber = setInterval(() => {
        this.incrementedNumber++; 
      }, 25);

      // after 2.5 seconds, the increment stops
      setTimeout(() => {
        clearInterval(increaseNumber);
      }, 2500);
    },
    checkPosition() {
      // check from the top to the bottom of the scroll the position of li.card-fact(by $ref) on the page
      const cardPosition = this.$refs.cardFact.getBoundingClientRect().top;
      // execute getIncreaseNumber if the li.card-fact is visible on the page
      if (cardPosition < window.innerHeight) { 
        this.getIncreaseNumber(); 
      }
    },
  },
  mounted(){
    window.addEventListener("scroll", this.checkPosition);
  }
}
</script>

<!-- FeatureFactsCardListItem -->
<template>
  <!-- li of the single card-fact(fact) -->
  <li ref="cardFact" class="card-fact">
    <!-- number of the fact that increases by the method: getIncreaseNumber() -->
    <h5>{{ incrementedNumber  }}</h5>
    <!-- title of the card -->
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