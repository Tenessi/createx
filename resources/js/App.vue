<template>
  <div class="app">
    <div class="container">
      <the-header />
      <the-main />
      <the-footer />
    </div>
  </div>
</template>

<script>
  import TheHeader from './components/header/TheHeader.vue';
  import TheMain from './pages/TheMain.vue';
  import TheFooter from './components/footer/TheFooter.vue'
  export default {
    components: {
      TheHeader,
      TheMain,
      TheFooter
    }

  }

</script>

<style>
  .app {
    font-family: 'Lato', sans-serif;
  }
  .container {
    margin: 0 auto;
    max-width: 1920px;
    width: 100%;
  }
</style>
