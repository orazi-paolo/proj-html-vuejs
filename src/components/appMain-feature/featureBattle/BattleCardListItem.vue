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
      <img class="img-versus" :src="getImagePath(imgUrlVersus)" :alt="imgUrlVersus">
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
      <a href="#">
        <img :src="getIconPath(imgUrlYoutube)" :alt="imgUrlYoutube">
        <span>Youtube</span>
      </a>
      <!-- icon of twitter -->
      <a href="#">
        <img :src="getIconPath(imgUrlTwitter)" :alt="imgUrlTwitter">
        <span>Twitch</span>
      </a>
    </div>
  </li>
</template>

<style lang='scss'scoped>
.card-battle{
  background-color: #fff;
  border: 2px solid #3B5171;
  overflow: hidden;
  border-radius: 20px;
  flex-basis: calc(50% - 20px/2);

  .battle, .info, .links{
    text-align: center;
  }

  .battle{
    padding: 40px 0;
    background-color: #283449;

    .img-versus{
      margin: 0 20px
    }
  }

  .info{
    padding: 30px 0;
    background-color: #2D405E;
   
    h4{
      color: #fff;
      margin-bottom: 20px;
    }
    p{
      color: #94CB53;
    }
  }

  .links{
    padding: 40px 0;
    background-color: #283449;
    color: #fff;
    
    a{
      text-decoration: none;
      img{
        margin-right: 5px;
      }
      span{
        color: #fff;
        margin-right: 25px;
      }
    }
  }
}
</style>