<template>
  <main>
    <JumboComponent />
    <div class="container">

        <CardComponent
            v-for="(comics, index) in ComicsBooks" 
            :key="`Comic-${index}`"
            :ComicElement="comics"
        />
    </div>
  </main>
</template>

<script>

import JumboComponent from './JumboComponent.vue'
import CardComponent from './CardComponent.vue'
import ComicsBooks from '../assets/data/ComicBooks'


export default {
    name: "MainComponent",
    components: { JumboComponent, CardComponent },
    data() {
        return{
            ComicsBooks
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/mixins';

main{
    background-color: #1C1C1C;
    .container{
        padding: 80px 0;
        @include displayCenter;
        flex-wrap: wrap;
        h1{
            color: white;
        }
    }
}
</style>