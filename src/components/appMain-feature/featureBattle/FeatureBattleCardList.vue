<script>
import AppMainFeatureBattleCardListItem from './BattleCardListItem.vue'

export default {
  data() {
    return {
      listBattles: [
        {
          imgUrlTeamOne:'game-img-1.png',
          imgUrlTeamTwo:'game-img-2.png',
          title:'Call Of Deauty',
        },
        {
          imgUrlTeamOne:'game-img-3.png',
          imgUrlTeamTwo:'game-img-4.png',
          title:'Legendary Battles',
        },
        {
          imgUrlTeamOne:'game-img-5.png',
          imgUrlTeamTwo:'game-img-6.png',
          title:'Nay Corral Gundown',
        },
        {
          imgUrlTeamOne:'game-img-7.png',
          imgUrlTeamTwo:'game-img-8.png',
          title:'League of Legends',
        },
      ]
    }
  },
  components:{
    AppMainFeatureBattleCardListItem
  }
}
</script>

<!-- FeatureBattleCardList -->
<template>
  <ul id="list-battles">
    <!-- sended by props to AppMainFeatureBattleCardListItem the items(battle) of listBattles[] with v-for-->
    <AppMainFeatureBattleCardListItem 
      v-for="(battle, index) in listBattles" :key="index" :battle="battle"
    />  
  </ul>
</template>

<style lang="scss" scoped>
  #list-battles{
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
  }

</style>
