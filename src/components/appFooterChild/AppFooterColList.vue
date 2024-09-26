<script>
export default {
  data() {
    return {
      
    }
  },
  props: {
    title: {
      type: String,
      required: true
    },
    items: {
      type: Array,
      required: true
    }
  }
}
</script>

<template>
  <div class="col-2">
    <h5 class="mb-3">
      {{ title }}
    </h5>
    <ul class="list-unstyled">
      <li v-for="item in items" :key="item" class="mb-2">
         <a href="">
            {{ item }}
         </a>
        </li>
    </ul>
  </div>
</template>

<style lang="scss" scoped>
li{
  a{
    color: rgba(211, 211, 211, 0.437);
    font-size: 14px;
    text-decoration: none;
    &:hover{
      color: #94CB53;
    }
  }
}
</style>