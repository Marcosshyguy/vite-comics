<script >
export default{
  data(){
    return {

    }
  },
  methods :{

  },
  components:{

  },
  props:{
    image:String,
    title: String,
    price: String
  }
}
</script>

<template>
  <div class="card">
    <img :src=image :alt="title">
    <p>{{title}}</p>
    <p>{{price}}</p>
  </div>
</template>

<style lang="scss" scoped>
@use "../styles/paertials/variables.scss" as *;
@use "../styles/paertials/mixins.scss" as *; 
.card{
    width: calc(100% / 6);
    display: flex;
    flex-direction: column;
    gap: .5em
}
</style>