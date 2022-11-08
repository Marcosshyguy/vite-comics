<script >
export default{
  data(){
    return {

    }
  },
  methods :{

  },
  components:{

  }
}
</script>

<template>
  <main>
    <div>
        <h1>some content here...</h1>
    </div>
  </main>
</template>

<style lang="scss" scoped>
@use "../styles/general.scss" as *;
@use "../styles/paertials/variables.scss" as *;
@use "../styles/paertials/mixins.scss" as *; 

main{
    background-color: black;
    color: white;

        div{
            @include page-centering(60%);
            padding: 2em 1em;
        }
}

</style>