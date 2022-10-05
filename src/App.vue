<template>
  <div id="app">
   <HeaderComponent />
   <JumboTronComponent />
   <MainComponent />
   <FooterComponent />
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import MainComponent from './components/MainComponent.vue';
import FooterComponent from './components/FooterComponent.vue';
import JumboTronComponent from './components/JumboTronComponent.vue';

export default {
  name: 'App',
  components: {
    HeaderComponent,
    MainComponent,
    FooterComponent,
    JumboTronComponent
}
}
</script>

<style lang="scss">
  @import './style/general_style.scss';
  @import './style/utilities.scss';

  #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>

