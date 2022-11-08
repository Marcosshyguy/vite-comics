<script >
export default{
  data(){
    return {
        merchList:[
            {
                name : 'Digital Comics',
                image : 'buy-comics-digital-comics.png'
            },
            {
                name : 'Dc Merchandise',
                image : 'buy-comics-merchandise.png'
            },
            {
                name : 'Subscription',
                image : 'buy-comics-subscriptions.png'
            },
            {
                name : 'Digital Comics',
                image : 'buy-comics-shop-locator.png'
            },
            {
                name : 'Digital Comics',
                image : 'buy-dc-power-visa.svg'
            }
        ]
    }
  },
  methods :{
    getImagePath(imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
  },
  components:{

  }
}
</script>

<template>
  <section>
        <div class="merch-container">
            <div v-for="(merch, merchIndex) in merchList" :key="merchIndex">
                <div>
                    <img :src="getImagePath(`../assets/img/${merch.image}`)" alt="">
                </div>
                <p>{{merch.name}}</p>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use "../styles/general.scss" as *;
@use "../styles/paertials/variables.scss" as *;
@use "../styles/paertials/mixins.scss" as *; 


section{
    background-color: $merch-bg;
    color: white;

    .merch-container{
        @include toUppercase();
        @include page-centering(60%);
        display: flex;
        justify-content: center;
        padding: 2em;
        gap: 1em;
        
        

        div{
            display: flex;
            align-items: center;
            gap: .5em;

            div{
                width: 40%;

                img{
                    width: 100%;
                    height: 100%;
                    object-fit:contain;
                }
            }
        }
    }
}
</style>