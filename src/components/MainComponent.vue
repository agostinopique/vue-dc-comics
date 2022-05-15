<template>
  <main>
    <div class="container">
        <h1>--->MAIN CONTENT&lt;---</h1>
    </div>
  </main>
</template>

<script>
export default {
    name: 'MainComponent'
}
</script>

<style lang="scss" scoped>
@import '../assets/style/mixins';

main{
    background-color: black;
    height: 150px;
    .container{
        height: 100%; 
        @include displayCenter;
        h1{
            color: white;
        }
    }
}
</style>