<template>
    <div class="container d-flex">
            <div class="list-section w-50 d-flex flex-wrap pt-3">
                <div>
                    <ul>
                        <h4 class="text-light pt-3">DC COMICS</h4>
                        <li>Characters</li>
                        <li>Comics</li>
                        <li>Movies</li>
                        <li>TV</li>
                        <li>Games</li>
                        <li>Videos</li>
                        <li>News</li>
                    </ul>
                    <ul>
                        <h4 class="text-light pt-3">SHOP</h4>
                        <li>Shop DC</li>
                        <li>Shop DC Collectibles</li>
                    </ul>
                </div>
                <ul>
                    <h4 class="text-light pt-3">DC</h4>
                    <li>terms of use</li>
                    <li>privacy policy (new)</li>
                    <li>ad choices</li>
                    <li>advertising</li>
                    <li>jobs</li>
                    <li>subscriptions</li>
                    <li>talent workshop</li>
                    <li>CPSC certificates</li>
                    <li>ratings</li>
                    <li>shop help</li>
                    <li>contact us</li>
                </ul>
                <ul>
                    <h4 class="text-light pt-3">SITE</h4>
                    <li>DC</li>
                    <li>MAD magazine</li>
                    <li>DC kids</li>
                    <li>DC universe</li>
                    <li>DC power visa</li>
                </ul>
            </div>
        <div class="footer-logo w-50"></div>
    </div>
</template>

<script>
export default {
    name: 'FooterTop'
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars';
@import '../assets/style/mixins';

.list-section,
.footer-logo {
    height: 450px;
}

.footer-logo{
    background-image: url(../assets/img/dc-logo-bg.png);
    background-position: center;
    background-size: cover;
}

.list-section ul{
    @include listItems;
    color: #868776;
    li{
        text-transform: capitalize;
        font-size: 14px;
        padding: 3px 0;
    }
}


</style>