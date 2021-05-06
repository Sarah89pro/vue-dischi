<template>
  <div id="app">
    <!--HEADER-->
    <Header/>
    <!--MAIN con nesting MAINCARDS-->
    <Main/>
    
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Main from './components/Main.vue';

export default {
  name: 'App',
  components: {
    Header,
    Main,
  },
};
</script>

<style lang="scss">


.container {
  width: 1200px;
  margin: 0 auto;
}

@import '@/styles/general';
@import '~@fontsource/roboto/index.css';
</style>
