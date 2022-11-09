<script >
export default{
    data(){
        return {
            logoImage : 'dc-logo.png',
            itemListHeader : [{
                    linkName : 'characters',
                    linkState : true
                },
                {
                    linkName : 'comics',
                    linkState : false
                },
                {
                    linkName : 'movies',
                    linkState : false
                },
                {
                    linkName : 'tv',
                    linkState : false
                }   
            ],
            currentIndexLink: 0
        }
    },
    methods :{
        getImagePath(imgPath) {
            return new URL(imgPath, import.meta.url).href;
        },
        linkSelected (currentIndex){
            this.itemListHeader[this.currentIndexLink].linkState = false;
            this.currentIndexLink = currentIndex;
            this.itemListHeader[this.currentIndexLink].linkState = true;
            
        }

    },
    components:{

    }
}
</script>

<template>
    <header>
        <div class="header-container">
            <div>
                <img :src="getImagePath(`../assets/img/${this.logoImage}`)" alt="">
            </div>
            <div class="header-list">
                <ul>
                    <li  
                    v-for="(link, linkIndex) in this.itemListHeader" 
                    :key="linkIndex"
                    :class="(link.linkState) ? 'underlined' : ''">
                        <a @click="linkSelected (linkIndex)" :class="(link.linkState) ? 'colored' : ''">{{link.linkName}}</a>
                    </li>
                </ul>
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use "../styles/general.scss" as *;
@use "../styles/paertials/variables.scss" as *;
@use "../styles/paertials/mixins.scss" as *; 

    header{
        height: $header-height;
        

            .header-container{
                @include page-centering(60%);
                height: 100%;
                display: flex;
                align-items: center;
                justify-content: space-between;

                div:first-child{
                    height: 80%;

                    img{
                        height: 100%;
                        width: 100%;
                        object-fit: cover;
                    }
                }

                div:last-child{
                    height: 100%;
                    ul{
                        @include toUppercase();
                        display: flex;
                        gap: 1em;
                        height: 100%;
                        
                        li{
                            
                            position: relative;
                            display: flex;
                            align-items: center;
                            
                            &.underlined::after{
                                // metodo per creare oggetto sottolineato senza crere spostamneto del contenuto causato dal border
                                content: "";
                                position: absolute;
                                bottom: 0;
                                left: 0;
                                display: inline-block;
                                width: 100%;
                                height: 5px;
                                background-color: $merch-bg;
                            }

                            a{
                                &:active{
                                    color: lighten(black, 80%);
                                }

                                &.colored{
                                    color: $merch-bg;
                                }
                                
                            }
                        }
                    }
                }
            }
    }

</style>