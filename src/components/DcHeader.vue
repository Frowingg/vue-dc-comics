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
                        <li> <a href="">CHARACTERS</a></li>
                        <li> <a href="">COMICS</a></li>
                        <li> <a href="">MOVIES</a></li>
                        <li> <a href="">TV</a></li>
                        <li> <a href="">GAMES</a></li>
                        <li> <a href="">COLLECTIBLES</a></li>
                        <li> <a href="">VIDEOS</a></li>
                        <li> <a href="">FANS</a></li>
                        <li> <a href="">NEWS</a></li>
                        <li> <a href="">SHOP</a></li>
                    </ul>
                </div>

            </div>
        </div>


    </header>
</template>

<script>

</script>

<style scoped>
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