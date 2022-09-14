<template>
  <div id="app">
    <Header/>
    <MainComponent/>
    <Footer/>
  </div>
</template>

<script>

import MainComponent from './components/MainComponent.vue';
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    MainComponent,
    Header,
    Footer
}
}
</script>

<style lang="scss">

  @import './style/general.scss'

</style>
