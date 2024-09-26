<script>
export default {
  data(){
    return{

    }
  },
  props:{
    item:{
      type: Object,
      Required: true
    }
  },
  components: {

  },
  methods: {
    getImagePath(img){
        return new URL(`../../../assets/icon/${img}`, import.meta.url).href
    }
  },
}
</script>

<!-- AppMainFeatureMakeYourMarkCardListItem -->
<template>
    <li class="card-gaming">
        <div class="box-icon">
            <img :src="getImagePath(item.imgUrl)" :alt="item.imgUrl">
        </div>
        <div class="box-info">
            <h3>{{ item.title }}</h3>
            <p>{{ item.description }}</p>
        </div>
    </li>
</template>

<style lang="scss" scoped>
    .card-gaming{
        display: flex;
        gap: 10px;
        
        
        .box-icon{
            flex-basis: 20%;
        }
        .box-info{
            flex-grow: 1;
        }
    }

</style>