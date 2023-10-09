<template>
  <header class="header">
    <header-top/>
    <header-main/>
  </header>
</template>

<script>
import HeaderTop from './header-components/HeaderTop.vue'
import HeaderMain from './header-components/HeaderMain.vue'
  export default {
    components: {
      HeaderTop,
      HeaderMain
    }
  }

</script>

<style lang="scss">
  .header {
    display: flex;
    flex-direction: column;
  }
</style>
