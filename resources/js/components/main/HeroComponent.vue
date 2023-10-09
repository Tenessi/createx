<template>
  <div class="hero__background">
    <img class="hero__background_image" src="/images/main/hero.jpg" alt="Background image">
  </div>
  <div class="hero">
    <h2 class="hero__upper-title">
      NEW COLLECTION
    </h2>
    <h1 class="hero__title">
      Menswear2020
    </h1>
    <div class="hero__buttons">
      <a href="" class="hero__buttons_item">Shop sale</a>
      <a href="" class="hero__buttons_item">Shop the menswear</a>
    </div>
  </div>
</template>

<script>

  export default {
    components: {
      
    }

  }

</script>

<style lang="scss">
  .hero {
    display: flex;
    flex-direction: column;
    max-width: 1260px;
    width: 100%;
    padding: 140px 15px;
    margin: 0 auto;   
    margin-bottom: 210px;
    &__background {
      position: absolute;
      width: 1920px;
      height: 800px;
      z-index: -10;
    }
    &__upper-title {
      font-size: 18px;
      font-weight: 700;
      line-height: 150%; 
      letter-spacing: 1px;
      color: #1E212C;
    }
    &__title {
      margin-top: 12px;
      font-size: 72px;
      font-weight: 900;
      line-height: 130%;
      letter-spacing: 1px;
      color: #1E212C;
    }
    &__buttons {
      display: flex;
      margin-top: 60px;
      &_item {
        padding: 0px 40px;
        font-size: 16px;
        font-weight: 700;
        line-height: 52px;
        letter-spacing: 0.5px;
        text-align: center;
        border-radius: 4px;
        border: 1px solid  #17696A;
        transition: all 0.3s ease-in-out;
      }
      &_item:first-child {
        background: none;
        color: #17696A;
      }
      &_item:last-child {
        margin-left: 24px;
        background: #17696A;
        color: #FFF;
      }
      &_item:first-child:hover {
        background: #17696A;
        color: #FFF;
      }
      &_item:last-child:hover {
        border: 1px solid #145C5D;
        background-color: #145C5D;
      }
    }
  }
</style>