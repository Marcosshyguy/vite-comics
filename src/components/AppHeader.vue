<script >
export default{
    data(){
        return {
            logoImage : 'dc-logo.png',
            itemListHeader : [{
                    headerLink : '/characters',
                    linkName : 'characters',
                    linkState : true
                },
                {
                    headerLink : '/comics',
                    linkName : 'comics',
                    linkState : false
                },
                {
                    headerLink : '/movies',
                    linkName : 'movies',
                    linkState : false
                },
                {
                    headerLink : '/tv',
                    linkName : 'tv',
                    linkState : false
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
    <header>
        <div class="header-container">
            <div>
                <img :src="getImagePath(`../assets/img/${logoImage}`)" alt="">
            </div>
            <div class="header-list">
                <ul>
                    <li v-for="(link, linkIndex) in this.itemListHeader" :key="linkIndex"><a href="">{{link.linkName}}</a></li>
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
                @include page-centering();
                height: 100%;
                display: flex;
                align-items: center;
                justify-content: space-between;

                div:first-child{
                    height: 90%;

                    img{
                        height: 100%;
                        width: 100%;
                        object-fit: cover;
                    }
                }

                div:last-child{

                    ul{
                        display: flex;
                        gap: 1em;
                    }
                }
            }
    }

</style>