<template>
    
    <div>

        <section id="jumbotron">
            <img src="../assets/img/jumbotron.jpg" alt="">
        </section>

        <section id="main-top">
            <div class="container">

                <div class="tag">
                    CURRENT SERIES
                </div>

               <DcComicCard v-for="(infoDet, index) in cardInfo" :key="index" :infoDet = 'cardInfo[index]' />

                <button id="main-top-btn">
                    LOAD MORE
                </button>

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
import DcComicCard from './DcComicCard.vue';
export default {
    name: 'DcMain',
    components: {
        DcComicCard
    },
    data() {
        return {
            cardInfo:[
                    {
                        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
                        "price": "$19.99",
                        "series": "Action Comics",
                        "type": "comic book"
                    },
                    {
                        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
                        "price": "$3.99",
                        "series": "American Vampire 1976",
                        "type": "comic book"
                    },
                    {
                        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
                        "price": "$16.99",
                        "series": "Aquaman",
                        "type": "graphic novel"
                    },
                    {
                        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
                        "price": "$2.99",
                        "series": "Batgirl",
                        "type": "comic book"
                    },
                    {
                        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                        "price": "$3.99",
                        "series": "Batman",
                        "type": "comic book"
                    },
                    {
                        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                        "price": "$2.99",
                        "series": "Batman Beyond",
                        "type": "comic book"
                    },
                    {
                        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
                        "price": "$3.99",
                        "series": "Batman/Superman",
                        "type": "comic book"
                    },
                    {
                        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
                        "price": "$4.99",
                        "series": "Batman/Superman Annual",
                        "type": "comic book"
                    },
                    {
                        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
                        "price": "$5.99",
                        "series": "Batman: The Joker War Zone",
                        "type": "comic book"
                    },
                    {
                        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
                        "price": "$6.99",
                        "series": "Batman: Three Jokers",
                        "type": "comic book"
                    },
                    {
                        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
                        "price": "$4.99",
                        "series": "Batman: White Knight Presents: Harley Quinn",
                        "type": "comic book"
                    },
                    {
                        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
                        "price": "$16.99",
                        "series": "Catwoman",
                        "type": "graphic novel"
                    }
                ],
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
@import '../style/variable.scss';
.container{
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}
#jumbotron{
    width: 100%;
    max-height: 300px;
    overflow: hidden;

    img{
        width: 100%;
        height: 100%;
    }
}
#main-top{
    background-color: #1c1c1c;
    padding: 40px 0 20px;
    .tag{
        position: relative;

        color: white;
        padding: 5px 10px;
        height: 30px;
        position: absolute;
        top: 46%;
        left: 17%;
        background-color: $brand-main-color;
        justify-self: flex-start;
    }
    #main-top-btn{
        background-color: $brand-main-color;
        padding: 10px 40px;
        border: none;
        color: white;
        cursor: pointer;
    }
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