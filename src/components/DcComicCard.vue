<template>

        <div class="card">
            <div class="card-img">
                <img :src="infoDet.thumb" alt="infoDet.series">
            </div>
            <p>{{ infoDet.series }}</p>
        </div>
        


</template>

<script>
export default {
    name: 'DcComicCard',
    props: {
        infoDet: Object
    }
}
</script>

<style lang="scss" scoped>
.card{
    width: calc(100% / 6 - 20px);
    max-height: 200px;
    margin-right: 20px;
    color: white;
    padding-bottom: 8px;
    .card-img{
        width: 100%;
        max-height: 70%;
        overflow: hidden;
    }
    img{
        width: 100%;
        height: 100%;
    }
    p{
        margin-top: 6px;
        font-size: 13px
    }
}

</style>