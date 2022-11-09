<script >
import AppHeroCard from './AppHeroCard.vue';

export default{
  data(){
    return {

    }
  },
  methods :{

  },
  components:{
    AppHeroCard
  }
}
</script>

<template>
  <main>
    <div>
      <AppHeroCard/>
    </div>
  </main>
</template>

<style lang="scss" scoped>

@use "../styles/paertials/variables.scss" as *;
@use "../styles/paertials/mixins.scss" as *; 

main{
    background-color: black;
    color: white;

        div{
            @include page-centering(60%);
            padding: 2em 0;
            display: flex;
            justify-content: flex-start;
        }
}

</style>