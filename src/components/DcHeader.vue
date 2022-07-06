<template>
    <header>

        <div class="container">
            <div id="header-left">
                <div id="logo">
                    <img src="../img/dc-logo.png" alt="">
                </div>
            </div>

            <div id="header-right">

                <div id="header-nav">
                    <ul>
                        <li v-for="(link, index) in menuLinks" :key="index" :class="{ 'current': link.current}">
                            <a :href="link.url"> {{ link.text }} </a>
                        </li>
                    </ul>
                </div>

            </div>
        </div>


    </header>
</template>

<script>
    export default {
        name: 'DcHeader',
        data() {
            return {
                menuLinks: [
                    {
                        text: 'CHARACTERS',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'COMICS',
                        url: '#',
                        current: true,
                    },
                    {
                        text: 'MOVIES',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'TV',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'GAMES',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'COLLECTIBLES',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'VIDEOS',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'FANS',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'NEWS',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'SHOP',
                        url: '#',
                        current: false,
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
    justify-content: space-between;
}
#logo{
    width: 60px;
    height: 60px;
    margin: 15px 0
}
img{
    width: 100%;
}
#header-nav{
    height: 100%;
}
ul{
    display: flex;
    height: 100%;
    margin: 0
}
li{
    margin: 0 10px;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 9px;
    font-weight: 300;
}
li:hover{
    border-bottom: 4px solid #0282f9;
}
li:hover a{
    color: #0282f9;
}
</style>