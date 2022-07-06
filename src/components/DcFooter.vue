<template>
    <div>
        
        <section id="footer-top">
            <div class="container">
                <div class="single-ul">

                    <ul>
                        <h3>DC COMICS</h3>
                        <li v-for="(link, index) in menuLinks1" :key="index">
                            <a :href="link.url"> {{ link.text }} </a>
                        </li>
                    </ul>

                </div>

                <div class="single-ul">

                    <ul>
                        <h3>SHOP</h3>
                        <li v-for="(link, index) in menuLinks2" :key="index">
                            <a :href="link.url"> {{ link.text }} </a>
                        </li>
                    </ul>
                    
                </div>

                <div class="single-ul">

                    <ul>
                        <h3>DC COMICS</h3>
                        <li v-for="(link, index) in menuLinks3" :key="index">
                            <a :href="link.url"> {{ link.text }} </a>
                        </li>
                    </ul>
                    
                </div>

                <div class="single-ul">

                    <ul>
                        <h3>DC COMICS</h3>
                        <li v-for="(link, index) in menuLinks3" :key="index">
                            <a :href="link.url"> {{ link.text }} </a>
                        </li>
                    </ul>
                    
                </div>
            </div>
        </section>

        <section id="footer-bottom"></section>

    </div>
</template>

<script>
    export default {
        name: 'DcFooter',
        data() {
            return{
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
                    },
                ],
                menuLinks2: [
                    {
                        text: 'Shop DC',
                        link: '#',
                    },
                    {
                        text: 'Shop DC Collectibles',
                        link: '#',
                    },
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>

#footer-top{
    height: 600px;
    background-image: url('../assets/img/footer-bg.jpg');
}
h3{
    color: white;
    padding: 10px 0;
}
a{
    color: gray;
    font-size: 11px;
    cursor: pointer;
}

</style>