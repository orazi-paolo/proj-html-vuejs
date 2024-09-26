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

<template>
  <li class="card-battle">
    <div class="battle">
      <img :src="getImagePath(battle.imgUrlTeamOne)" :alt="battle.imgUrlTeamOne">
      <img :src="getImagePath(imgUrlVersus)" :alt="imgUrlVersus">
      <img :src="getImagePath(battle.imgUrlTeamTwo)" :alt="battle.imgUrlTeamOne">
    </div>
    <div class="info">
      <h4>{{ battle.title }}</h4>
      <p>December 25, 2022 4:00 PM</p>
    </div>
    <div class="links">
      <img :src="getIconPath(imgUrlYoutube)" :alt="imgUrlYoutube">
      <span>Youtube</span>
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