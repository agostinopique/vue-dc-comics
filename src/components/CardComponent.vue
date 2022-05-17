<template>
    <div class="card-box">
        <div class="card-container">
            <div class="cardItem">
                <img :src="ComicElement.thumb" :alt="ComicElement.series">
            </div>
            <span class="comic-title text-light">{{ComicElement.series}}</span>
        </div>
    </div>
</template>

<script>
export default {
    name: 'CardComponent',
    props: {
        ComicElement: Object
    }
}
</script>

<style lang="scss" scoped>

.card-box{
    height: 280px;
    padding: 15px;
    .card-container{
        width: 160px;
    }
    .cardItem{
        height: 160px;
        border-radius: 3px;
        overflow: hidden;
        img{
            width: 100%;
        }
    }
    .comic-title{
        display: inline-block;
        text-transform: uppercase;
        margin-top: 15px;
    }
}
</style>