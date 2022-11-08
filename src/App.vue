<script >
import AppHeader from './components/AppHeader.vue';
import AppMainContent from './components/AppMainContent.vue';
import AppMerchSect from './components/AppMerchSect.vue';
export default{
  data(){
    return {

    }
  },
  methods :{

  },
  components:{
    AppHeader,
    AppMainContent,
    AppMerchSect
  }
}
</script>

<template>
  
  <AppHeader/>
  <AppMainContent/>
  <AppMerchSect/>
</template>

<style lang="scss">
@use "./styles/general.scss" as *;
@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap');
</style>
