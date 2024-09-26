<script>
export default {
  data() {
    return {
      imgUrlVersus:'verus-icon.png'
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
    }
  }
}
</script>

<template>
  <li class="card-battle">
    <img :src="getImagePath(battle.imgUrlTeamOne)" :alt="battle.imgUrlTeamOne">
    <img :src="getImagePath(imgUrlVersus)" :alt="imgUrlVersus">
    <img :src="getImagePath(battle.imgUrlTeamTwo)" :alt="battle.imgUrlTeamOne">
  </li>
</template>

<style scoped>
.card-battle{
  background-color: #fff;
}
</style>