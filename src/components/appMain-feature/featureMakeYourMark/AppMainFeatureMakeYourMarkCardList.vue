<script>
import AppMainFeatureMakeYourMarkCardListItem from './AppMainFeatureMakeYourMarkCardListItem.vue'

export default {
  data(){
    return{
        listGaming:[
            {
                title: 'Live Streaming',
                description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labor.',
                imgUrl: 'features-icon-1.png'
            },
            {
                title: 'Great Tournament',
                description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labor.',
                imgUrl: 'features-icon-2.png'
            },
            {
                title: 'Gaming News',
                description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labor.',
                imgUrl: 'features-icon-3.png'
            }
        ]
    }
  },
  components: {
    AppMainFeatureMakeYourMarkCardListItem,
  },
  methods: {

  },
}
</script>

<!-- AppMainFeatureMakeYourMarkCardList -->
<template>
    <!-- list-gaming with v-for and props sended -->
    <ul id="list-gaming">
        <!-- sended by props to AppMainFeatureMakeYourMarkCardListItem the items of listGaming[] with v-for-->
        <AppMainFeatureMakeYourMarkCardListItem 
            v-for="(item, index) in listGaming" :key="index" :item="item"
        />
    </ul>
</template>

<style lang="scss">

 #list-gaming{
    list-style-type: none;
    padding-left: 0;
 }

</style>