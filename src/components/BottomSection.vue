<template>
    <section>
        <div class="container">
                <ul>

                    <li v-for="(item, index) in bottomItems" :key="`bottom-item-${index}`">
                        <img :src="item.img" :alt="item.alt">
                        <a href="#">{{item.name}}</a>
                    </li>

                </ul>

        </div>
    </section>
</template>

<script>
/* 
import digitalComics from '../assets/img/buy-comics-digital-comics.png';
import dcMerchandise from '../assets/img/buy-comics-merchandise.png';
import subscription from '../assets/img/buy-comics-subscriptions.png';
import shopLocator from v;
import powerVisa from '../assets/img/buy-dc-power-visa.svg';
 */

export default {
    name: 'BottomComponent',
    data(){
        return{
            bottomItems: [

                {
                    name: 'Digital comics',
                    img: require('../assets/img/buy-comics-digital-comics.png'),
                    alt: 'digital-comics'
                },
                {
                    name: 'dc merchandise',
                    img: require('../assets/img/buy-comics-merchandise.png'),
                    alt: 'dc-merchandise'
                },
                {
                    name: 'subscription',
                    img: require('../assets/img/buy-comics-subscriptions.png'),
                    alt: 'subscription'
                },
                {
                    name: 'comic shop locator',
                    img: require('../assets/img/buy-comics-shop-locator.png'),
                    alt: 'shop-locator'
                },
                {
                    name: 'dc power visa',
                    img: require('../assets/img/buy-dc-power-visa.svg'),
                    alt: 'power-visa'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars';
@import '../assets/style/mixins';

section{
    height: 150px;
    background-color: $dc-blue;
}
.container{
    height: 100%;
}

ul{
    @include alignCenter;
    justify-content: space-between;
    padding-left: 0;
    @include listItems;
    height: 100%;
    li{
        @include alignCenter;
        width: calc(100% / 5);
        a{
            @include aLink;
            text-transform: uppercase;
            color: white;
        }
        img{
            max-width: 55px;
            max-height: 55px;
            margin-right: 10px;
        }
        
        
    }
}

</style>