<template>
  <header>
    <div class="container">
      <div class="logo">
          <img src="../assets/img/dc-logo.png" alt="dc-logo">
      </div>
      <nav>
        <ul>

          <li v-for="(item, index) in menuItems" :key="`menu-item-${index}`">
            <a :class="{'active' : item.isActive}" href="#">{{item.name}}</a>
          </li>

        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: 'HeaderComponent',
  data(){
    return{
      menuItems: [
        {
          name: 'Characters',
          isActive: false
        },
        {
          name: 'Comics',
          isActive: true
        },
        {
          name: 'Movies',
          isActive: false
        },
        {
          name: 'tv',
          isActive: false
        },
        {
          name: 'games',
          isActive: false
        },
        {
          name: 'collectibles',
          isActive: false
        },
        {
          name: 'videos',
          isActive: false
        },
        {
          name: 'fans',
          isActive: false
        },
        {
          name: 'news',
          isActive: false
        },
        {
          name: 'shop',
          isActive: false
        }
      ]
    }
  }
}
</script>

<style lang='scss' scoped>
@import '../assets/style/vars';
@import '../assets/style/mixins';

header{
  height: 100px;
}

.container{
  display: flex;
  justify-content: space-between;
}

.logo{
  height: 100px;
  width: 100px;
  padding: 10px;
  img{
    width: 100%;
  }
}

nav{
  display: flex;
  align-items: center
}

ul{
  @include listItems;
  display: flex;
  align-items: center;
  margin-bottom: none;
  li a{
    @include aLink();
    display: inline-block;
    text-transform: uppercase;
    padding: 37px 15px 35px 15px;
    border-bottom: 4px solid white;
    color: black;

    &.active{
      border-color: $dc-blue;
      color: $dc-blue;
    }
  }
}
</style>