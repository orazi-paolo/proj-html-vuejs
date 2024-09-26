<script>
export default {
  data() {
    return {
      imgUrlVersus:'verus-icon.png',
      imgUrlYoutube:'youtube-icon.png',
      imgUrlTwitter:'twitch-icon.png',
    }
  },
  props:{
    battle:{
      required: true,
      type: Object,
    }
  },
  methods:{
    getImagePath(img){
        return new URL(`../../../assets/${img}`, import.meta.url).href
    },
    getIconPath(icon){
        return new URL(`../../../assets/icon/${icon}`, import.meta.url).href
    }
  }
}
</script>

<!-- BattleCardListItem -->
<template>
  <!-- li of the single card-battle(battle) -->
  <li class="card-battle">
    <!-- top-section of card-battle -->
    <div class="battle">
      <!-- img of the first team -->
      <img :src="getImagePath(battle.imgUrlTeamOne)" :alt="battle.imgUrlTeamOne">
      <!-- img 'vs' -->
      <img :src="getImagePath(imgUrlVersus)" :alt="imgUrlVersus">
      <!-- img of the second team -->
      <img :src="getImagePath(battle.imgUrlTeamTwo)" :alt="battle.imgUrlTeamOne">
    </div>

    <!-- mid-section of card-battle -->
    <div class="info">
      <!-- name of the battle(title) -->
      <h4>{{ battle.title }}</h4>
      <!-- date of the battle -->
      <p>December 25, 2022 4:00 PM</p>
    </div>

    <!-- bottom-section of card-battle -->
    <div class="links">
      <!-- icon of youtube -->
      <img :src="getIconPath(imgUrlYoutube)" :alt="imgUrlYoutube">
      <span>Youtube</span>
      <!-- icon of twitter -->
      <img :src="getIconPath(imgUrlTwitter)" :alt="imgUrlTwitter">
      <span>Twitch</span>
    </div>
  </li>
</template>

<style scoped>
.card-battle{
  background-color: #fff;
  flex-basis: calc(50% - 20px/2);
}
</style>