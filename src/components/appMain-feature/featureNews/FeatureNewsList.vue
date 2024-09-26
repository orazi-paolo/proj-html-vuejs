<script>
import FeatureNewsListCard from './FeatureNewsListCard.vue'
export default {
  data() {
    return {
      // set the value of the cards with an array of objects
      littleCards: [
        { 
          image:  new URL('../../../assets/blog-item-2.png', import.meta.url).href, 
          title: 'Top 5 Most Important Aspects Of Your Game',
          clock: '10 Min',
          visual: '240',
          date: 'Apr 11, 2022' 
        },
        { 
          image: new URL("../../../assets/blog-item-3.png", import.meta.url).href, 
          title: 'The Rise Of Fantasy Sports And Online Games',
          clock: '10 Min',
          visual: '240',
          date: 'Apr 11, 2022'
        },
        { 
          image: new URL("../../../assets/blog-item-4.png", import.meta.url).href, 
          title: 'Benefits Of Gaming - PC And Video Games',
          clock: '10 Min',
          visual: '240',
          date: 'Apr 11, 2022'
        }
      ],
      mainCard: {
        image: new URL("../../../assets/blog-item-1.png", import.meta.url).href,
        title: 'Secrets To An Amazing Role Playing Game',
        clock: '10 Min',
        visual: '240',
        date: 'Apr 11, 2022'
      }
    }
  },
  components: {
    FeatureNewsListCard
  },
}
</script>

<template>
   <div class="container py-4">
    <div class="row">
      <!-- Main card -->
      <div class="col-7 mb-4">
        <div class="card-news text-white">
            <img :src="mainCard.image" :alt="mainCard.title">
            <div class="card-body p-4">
              <div class="card-news-subtitle mb-3" >
                <span class="pe-5"><span><img class="pe-2" src="../../../assets/icon/clock.png" alt="icon clock"></span>{{ mainCard.clock }}</span>
                <span class="pe-5"><span><img class="pe-2" src="../../../assets/icon/eye.png" alt="icon eye"></span>{{ mainCard.visual }}</span>
                <span class="pe-5"><span><img class="pe-2" src="../../../assets/icon/calendar.png" alt="icon calendar"></span> {{ mainCard.date }}</span>
              </div>
              <h4 class="card-title text-white">{{ mainCard.title }}</h4>
            </div>
        </div>
      </div>
      <!-- I use a new component for the three similar cards -->
      <div class="col-5">
        <!-- Through props, I send all the necessary data to the underlying cards and use a v-for to loop through the array created earlier -->
        <FeatureNewsListCard v-for="(card,index) in littleCards" 
        :key="index"
        :title="card.title"
        :image="card.image"
        :clock="card.clock"
        :visual="card.visual"
        :date="card.date"/>
      </div>
    </div>
   </div>
</template>

<style lang="scss" scoped>
.card-news{
  background-color: #30405F;
  border-radius: 20px;
  min-height: 400px;
}
.card-news-subtitle{
  color: #94CB53;
}
.card-news>img{
  width: 100%;
  object-fit: cover;
}
</style>