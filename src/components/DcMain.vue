<template>
    
    <div>

        <section id="main-top">
            <div class="container">
               <p> --> Content goes here  </p>
            </div>
        </section>
            
        <section id="main-bottom">

            <div class="container">

                <ul>
                    <li v-for="(link, index) in menuLinks" :key="index">
                        <img :src="link.img" alt="img">
                        <p>{{link.text}}</p>
                    </li>
                </ul>

            </div>

        </section>

    </div>


</template>

<script>
    export default {
        name: 'DcMain',
        data() {
            return {
            menuLinks: [
                {
                    img: require('../assets/img/buy-comics-digital-comics.png'),
                    text: 'DIGITAL COMICS',
                },
                {
                    img:  require('../assets/img/buy-comics-merchandise.png'),
                    text: 'DC MERCHANDISE',
                },
                {
                    img:  require('../assets/img/buy-comics-subscriptions.png'),
                    text: 'SUBSCRIPTION',
                },
                {
                    img:  require('../assets/img/buy-comics-shop-locator.png'),
                    text: 'COMIC SHOP LOCATOR',
                },
                {
                    img:  require('../assets/img/buy-dc-power-visa.svg'),
                    text: 'DC POWER VISA',
                },
            ]
        }
        }
    }

</script>

<style lang="scss" scoped>
#main-top{
    background-color: black;
    height: 100px;
}
#main-bottom{
    background-color: #0282f9;
    height: 130px;
    display: flex;
    align-items: center;

}
p{
    color: white;
}
ul{
    display: flex;
    justify-content: space-between;
}
li{
    display: flex;
    align-items: center;
    font-size: 13px;

    img {
        width: 40px;
        margin: 0 10px 0 20px;
    }
}
</style>