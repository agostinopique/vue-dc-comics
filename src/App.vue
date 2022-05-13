<template>
  <div>
    <HeaderComponent />
    <MainComponent />
    <BottomSection />
    <FooterComponent />
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue'
import MainComponent from './components/MainComponent.vue'
import BottomSection from './components/BottomSection.vue'
import FooterComponent from './components/FooterComponent.vue'


export default {
  name: 'App',
  components: {
    HeaderComponent,
    MainComponent,
    BottomSection,
    FooterComponent
  }
}
</script>

<style lang="scss">
@import './assets/style/general';
</style>
