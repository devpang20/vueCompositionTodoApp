<template>
  <div id="app">
      <Main />
      <Footer />
    <Info />
  </div>
</template>

<script>
import Footer from './components/Footer.vue';
import Header from './components/Header.vue';
import Info from './components/Info.vue';
import Main from './components/Main.vue';

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer,
    Info,
  }
}
</script>

<style>
</style>
