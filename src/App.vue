<script>
import HeaderApp from './components/HeaderApp.vue';
import MainApp from './components/MainApp.vue';
import FooterApp from './components/FooterApp.vue';
export default {
  components: {
    HeaderApp,
    MainApp,
    FooterApp
  }
}
</script>
<template lang="">
  <div>
    <header>
      <HeaderApp />
    </header>
    <main>
      <MainApp />
    </main>
    <footer>
      <FooterApp />
    </footer>
  </div>
</template>
<style lang="scss">
  @use './styles/general.scss' as *;
  .container{
    width: 80%;
    max-width: 1200px;
    margin: 0 auto;
}
</style>