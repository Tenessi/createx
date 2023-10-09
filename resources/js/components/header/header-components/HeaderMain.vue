<template>
  <div class="header__main">
    <img src="/images/header/logo.svg" alt="Logo">
    <nav class="header__nav">
      <ul class="header__nav_list">
        <a class="header__nav_link" v-for="item in nav" v-bind:key="item.id" href="#">{{ item.title }}</a>
      </ul>
    </nav>
    <div class="header__input-block">
      <input class="header__input" type="text" placeholder="Search for products...">
      <img class="header__input_search" src="/images/header/search.svg" alt="Search">
    </div>
    <div class="header__toolbar">
      <div class="header__liked">
        <img class="header__liked_image" src="/images/header/heart.svg" alt="Liked">
        <span class="header__liked_quantity">2</span>
      </div>
      <div class="header__cart">
        <img class="header__cart_image" src="/images/header/cart.svg" alt="Cart">
        <span class="header__cart_quantity">4</span>
      </div>
    </div>
  </div>  
</template>

<script>
  export default {
    data() {
      return {
        nav: [
          {id: 1, title: 'Women'}, 
          {id: 2, title: 'Men'},
          {id: 3, title: 'Girls'},
          {id: 4, title: 'Boys'},
          {id: 5, title: 'Sale'}
        ]
      }
    },
  }
  
</script>

<style lang="scss">
  .header {
    &__main {
      max-width: 1260px;
      width: 100%;
      height: 85px;
      padding: 0px 15px;
      margin: 0 auto;   
      display: flex; 
      justify-content: space-between; 
      align-items: center;
    }
    &__nav {
      max-width: 350px;
      width: 100%;
      &_list {
        display: flex;
        justify-content: space-between;
        width: 100%;
      }
      &_link {
        font-size: 16px;
        font-weight: 700;
        line-height: 160%;
        color:#424551;
      }
      &_link:last-child {
        color: #FF4242;
      }
    }
    &__input-block {
      position: relative;
      max-width: 380px;
      width: 100%;
      height: 44px;

    }
    &__input {
      position: absolute;
      width: 100%;
      display: flex;
      justify-content: center;
      padding: 11px 16px 12px 16px;
      align-items: center;
      border-radius: 4px;
      border: 1px solid #D7DADD;
      font-size: 14px;
      font-weight: 400;
      line-height: 150%;
      color: #9A9CA5;
      background: #FFF;
      &_search {
        position: absolute;
        width: 16px;
        height: 16px;
        top: 50%;
        margin-top: -8px;
        right: 0;
        margin-right: 14px;
      }
    }
    &__toolbar {
      display: flex;
      justify-content: space-between;
    }
    &__liked {
      display: flex;
      padding-right: 20px;
      border-right: 1px solid #b3b6c5;
      cursor: pointer;
      &_quantity {
        margin-left: 8px;
        font-size: 16px;
        font-weight: 400;
        line-height: 160%;
        color: #424551;
      }
    }
    &__cart {
      display: flex;
      padding-left: 20px;
      cursor: pointer;
      &_quantity {
        display: flex;
        margin: 1px 0px 1px 8px;
        padding: 1px 8px;
        align-items: center;
        font-size: 12px;
        font-weight: 900;
        line-height: 150%;
        border-radius: 4px;
        background: #03CEA4;
        color: #FFF;
      }
    }
    
  }
</style>