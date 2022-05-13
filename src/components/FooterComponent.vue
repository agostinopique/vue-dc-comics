<template>
    <footer>
        
        <div class="footer-top">
            <FooterTop />
        </div>

        <div class="footer-bottom">
                <FooterBottom />
        </div>

    </footer>
</template>

<script>

import FooterTop from "./FooterTop.vue";
import FooterBottom from "./FooterBottom.vue";

export default {
    components: { FooterTop, FooterBottom }
}

</script>

<style lang="scss" scoped>

footer{
    height: 550px;
}

.footer-top {
    height: 450px;
    background-image: url(../assets/img/footer-bg.jpg);
    background-position: center;
    background-size: cover;
}

.footer-bottom{
    background-color: #303030;
    height: 100px;
}
</style>