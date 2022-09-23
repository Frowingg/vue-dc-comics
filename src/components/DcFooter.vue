<template>
    <footer>
        
        <section id="footer-top">
            <div class="container">
                <div id="footer-top-left">
                    <div class="col first-col-ul">

                        <ul>
                            <h3>DC COMICS</h3>
                            <li v-for="(link, index) in menuLinks1" :key="index" :link = 'menuLinks1[index]'>
                                <a :href="link.url"> {{ link.text }} </a>
                            </li>
                        </ul>
                        <ul>
                            <h3>SHOP</h3>
                            <li v-for="(link, index) in menuLinks2" :key="index">
                                <a :href="link.url"> {{ link.text }} </a>
                            </li>
                        </ul>

                    </div>

                    <div class="col second-col-ul">

                        <ul>
                            
                            <h3>DC</h3>
                            <li v-for="(link, index) in menuLinks3" :key="index">
                                <a :href="link.url"> {{ link.text }} </a>
                            </li>
                        
                        </ul>
                        
                    </div>

                    <div class="col third-col-ul">

                        <ul>
                            <h3>SITES</h3>
                            <li v-for="(link, index) in menuLinks4" :key="index">
                                <a :href="link.url"> {{ link.text }} </a>
                            </li>
                        </ul>
                    </div>
                
                </div>        

                <div id="footer-top-right">
                    <img src="../assets/img/dc-logo-bg.png" alt="logo-bg">
                </div>
            </div>

        </section>

        <section id="footer-bottom">

            <div class="container">

                <div id="footer-bottom-left">
                    <button id="footer-btn">
                        SIGN-UP NOW!
                    </button>
                </div>

                <div id="footer-bottom-right">
                    <h4>FOLLOW US</h4>
                    <ul v-for="(link, index) in iconMenuLinks" :key="index">
                        <li><img :src="link.img" alt=""></li>

                    </ul>
                </div>
            
            </div>

        </section>

    </footer>
</template>

<script>
export default {
    name: 'DcFooter',
    data() {
        return {
                menuLinks1: [
                {
                    text: 'Character',
                    link: '#',
                },
                {
                    text: 'Comics',
                    link: '#',
                },
                {
                    text: 'Movies',
                    link: '#',
                },
                {
                    text: 'Tv',
                    link: '#',
                },
                {
                    text: 'Games',
                    link: '#',
                },
                {
                    text: 'Videos',
                    link: '#',
                },
                {
                    text: 'News',
                    link: '#'
                }
                ],
            menuLinks2: [
                {
                    text: 'Shop DC',
                    link: '#',
                },
                {
                    text: 'Shop DC Collectibles',
                    link: '#',
                }
            ],
            menuLinks3: [
                {
                    text: 'Terms of Use',
                    link: '#',
                },
                {
                    text: 'Privacy Policy (New)',
                    link: '#',
                },
                {
                    text: 'Add Choice',
                    link: '#',
                },
                {
                    text: 'Advertising',
                    link: '#',
                },
                {
                    text: 'Jobs',
                    link: '#',
                },
                {
                    text: 'Subscriptions',
                    link: '#',
                },
                {
                    text: 'Talent Workshop',
                    link: '#',
                },
                {
                    text: 'CPSC Certificates',
                    link: '#',
                },
                {
                    text: 'Ratings',
                    link: '#',
                },
                {
                    text: 'Shop Help',
                    link: '#',
                },
                {
                    text: 'Contact Us',
                    link: '#',
                }
            ],
            menuLinks4: [
                {
                    text: 'DC',
                    link: '#',
                },
                {
                    text: 'MAD Magazine',
                    link: '#',
                },
                {
                    text: 'DC Kids',
                    link: '#',
                },
                {
                    text: 'DC Universe',
                    link: '#',
                },
                {
                    text: 'DC Power Visa',
                    link: '#',
                }
            ],    
            iconMenuLinks: [
                {
                    img: require('../assets/img/footer-facebook.png'),
                    link: '#'                    
                },
                {
                    img: require('../assets/img/footer-twitter.png'),
                    link: '#'                    
                },
                {
                    img: require('../assets/img/footer-youtube.png'),
                    link: '#'                    
                },
                {
                    img: require('../assets/img/footer-periscope.png'),
                    link: '#'                    
                },
                {
                    img: require('../assets/img/footer-pinterest.png'),
                    link: '#'                    
                },
            ], 
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../style/variable.scss';
footer{
    display: flex;
    flex-direction: column;
}

#footer-top{

    background-image: url('../assets/img/footer-bg.jpg');
    height: 330px;


    h3{
    color: white;
    padding: 10px 0;
    }
    a{
        color: gray;
        font-size: 11px;
        cursor: pointer;
    }
    .container{
        display: flex;
        justify-content: space-between;
    }
    #footer-top-left{
        display: flex;
        padding: 20px 0;
    }
    .col{
       margin-right: 40px;
    }
    #footer-top-right{
        
        img{
            width: 470px;
            z-index: 1;
            position: relative;
            top: -60px;
        }
    }
}
#footer-bottom{
    background-color: #303030;
    height: 100px;
    z-index: 2;

    .container{
        height: 100%;
        display: flex;
        justify-content: space-between;
        align-items: center;

        #footer-bottom-left{

            #footer-btn{
                padding: 5px 10px;
                border: 2px solid $brand-main-color;
                background-color: #303030;
                color: white
            }

        }

        #footer-bottom-right{

            display: flex;

            h4{
                color: $brand-main-color;
                margin-right: 20px
            }
            li{
                margin-right: 15px
            }
            img{
                width: 25px
            }
        }
    }
}
</style>