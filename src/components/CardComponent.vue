<template>
    <div class="card-container">
        <div class="cardItem">
            <img :src="ComicElement.thumb" :alt="ComicElement.series">
        </div>
        <span class="comic-title text-light">{{ComicElement.series}}</span>
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
.card-container{
    width: calc(100% / 6);
    height: 280px;
    padding: 15px;
    .cardItem{
        height: calc(90vh / 6);
        border-radius: 3px;
        overflow: hidden;
        img{
            width: 100%;
        }
    }
    .comic-title{
        display: inline-block;
        margin-top: 15px;
    }
}
</style>