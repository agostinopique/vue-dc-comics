<template>
    <section>
        <div class="container">
                <ul>
                    <li>
                        LIST ITEM
                    </li>
                    <li>
                        LIST ITEM
                    </li>
                    <li>
                        LIST ITEM
                    </li>
                    <li>
                        LIST ITEM
                    </li>
                    <li>
                        LIST ITEM
                    </li>
                </ul>

        </div>
    </section>
</template>

<script>
export default {
    name: 'BottomComponent'
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
    display: flex;
    justify-content: space-evenly;
    align-items:center;
    @include listItems;
    height: 100%;
    li{
        color: white;
    }
}

</style>