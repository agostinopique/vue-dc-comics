<template>
    <div class="container">
        <div class="cta-button">
            <a href="#">SIGN UP NOW!</a>
        </div>
        <div class="dc-social">
            <h3>FOLLOW US</h3>
            <ul>
                <li>
                    <a href="#">
                        <img src="../assets/img/footer-facebook.png" alt="dc-facebook">
                    </a>
                </li>
                <li>
                    <a href="#">
                        <img src="../assets/img/footer-twitter.png" alt="dc-twitter">
                    </a>
                </li>
                <li>
                    <a href="#">
                        <img src="../assets/img/footer-youtube.png" alt="dc-youtube">
                    </a>
                </li>
                <li>
                    <a href="#">
                        <img src="../assets/img/footer-pinterest.png" alt="dc-pinterest">
                    </a>
                </li>
                <li>
                    <a href="#">
                        <img src="../assets/img/footer-periscope.png" alt="dc-periscope">
                    </a>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    name: 'FooterBottom'
}
</script>

<style lang="scss" scoped>
@import '../assets/style/mixins';
@import '../assets/style/vars';

.container {
    height: 100px;
    @include alignCenter;
    justify-content: space-between;
}

.cta-button a{
    @include aLink;
    padding: 10px;
    color: white;
    border: 2px solid $dc-blue;
}

.dc-social {
    @include alignCenter;
}

.dc-social h3{
    color: $dc-blue;
    margin-bottom: 0;
}

.dc-social ul{
    @include listItems;
    display: flex;
    margin: 0;
    & a{
        @include aLink;
        margin: 0 8px;
    }
}
</style>