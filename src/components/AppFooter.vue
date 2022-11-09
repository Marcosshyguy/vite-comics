<script >
export default{
  data(){
    return {
        dcComicsList:["Characters","Comics","Movies","TV","Games","Videos","News"],
        shopsList:["Shop DC","Shop DC Collectibles"],
        DcList:["Terms Of Use","Privacy Policy(News)","Ad Choices","Advertising","Jobs","Subscriptions","Talent Workshop","CPSC Certificates","Ratings","Shop Help","Contact Us"],
        sitesList:["DC","MAD Magazine","DC Kids","DC Universe","Dc Power Visa"]
    }
  },
  methods :{

  },
  components:{

  }
}
</script>

<template>
  <footer>
    <div class="container">
        <div class="footer-top">
            <div>
                <h3><strong>DC COMICS</strong></h3>
                <ul>
                    <li v-for="(element1, index) in dcComicsList">
                        <a href="">{{element1}}</a>
                    </li>
                </ul>
                <h3><strong>SHOP</strong></h3>
                <ul>
                    <li v-for="(element2, index) in shopsList">
                        <a href="">{{element2}}</a>
                    </li>
                </ul>
            </div>
            <div>
                <h3><strong>DC</strong></h3>

                <ul>
                    <li v-for="(element3, index) in DcList">
                        <a href="">{{element3}}</a>
                    </li>
                </ul>
            </div><div>
                <h3><strong>SITES</strong></h3>
                <ul>
                    <li v-for="(element4, index) in sitesList">
                        <a href="">{{element4}}</a>
                    </li>
                </ul>
            </div>
        </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
@use "../styles/paertials/variables.scss" as *;
@use "../styles/paertials/mixins.scss" as *; 

footer{
    width: 100%;
    background-image: url(../assets/img/footer-bg.jpg);

        .footer-top{
            width: 100%;
            color: white;
            display: flex;
            justify-content: flex-start;
            gap: 1em;

                a{
                    color: white;

                }
        }
}
</style>