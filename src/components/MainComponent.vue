<template>
    <main>
        <JumboComponent />

        <div class="container">
            <div class="currentSeries">
                <h3 class="text-light">Current Series</h3>
            </div>
            <CardComponent 
                v-for="(comic, index) in ComicBooks"
                :key="`comic-${index}`"
                :ComicElement="comic" 
            />
        </div>
            <div class="loadMore">
                <a class="text-light" href="#">Load More</a>
            </div>

    </main>
</template>

<script>

import JumboComponent from './JumboComponent.vue'
import CardComponent from './CardComponent.vue'
import ComicBooks from '../assets/data/ComicBooks'



export default {
    name: "MainComponent",
    components: { JumboComponent, CardComponent },
    data() {
        return{
            ComicBooks
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/mixins';
@import '../assets/style/vars';

main{
    background-color: #1C1C1C;
    .container{
        padding: 80px 0;
        @include displayCenter;
        flex-wrap: wrap;
        position: relative;
    }
    .currentSeries{
        background-color: $dc-blue;
        padding: 8px 25px 4px 25px;
        position: absolute;
        top: -22px;
        left: 0;
        border-right: 1px solid black;
        h3{
            text-transform: uppercase;
        }
    }
    .loadMore{
        background-color: $dc-blue;
        padding: 8px 45px;
        width: 200px;
        position: relative;
        bottom: 40px;
        left: 50%;
        transform: translate(-50%);
        a{
            @include aLink;
            text-transform: uppercase;
            font-weight: bold;
        }
    }
}
</style>