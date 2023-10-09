<template>
  <main>
    <hero-component />
    <categories-component />
  </main>
</template>

<script>
  import HeroComponent from '../components/main/HeroComponent.vue';
  import CategoriesComponent from '../components/main/CategoriesComponent.vue';
  export default {
    components: {
      HeroComponent,
      CategoriesComponent
    }

  }

</script>

<style lang="scss">

</style>
