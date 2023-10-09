<template>
  <div class="header__top">
    <div class="header__container">
      <div class="header__access header__text">
        Available 24/7 at (405) 555-0128
      </div>
      <nav class="header__nav">
        <ul class="header__nav_list">
          <li v-for="item in nav" v-bind:key="item.id" class="header__nav_item header__text">{{ item.title }}</li>
        </ul>
      </nav>
      <div class="header__login header__text">
        Log in / Register
      </div>
    </div>
  </div>  
</template>

<script>
  export default {
    data() {
      return {
        nav: [
          {id: 1, title: 'Delivery & returns'}, 
          {id: 2, title: 'Track order'},
          {id: 3, title: 'Blog'},
          {id: 4, title: 'Contacts'}
        ]
      }
    },
  }
  
</script>

<style lang="scss">
  .header {
    &__top {
      height: 44px;
      background-color: #1E212C;
    }
    &__container { 
      display: flex; 
      justify-content: space-between; 
      height: 100%;
      align-items: center;
      max-width: 1260px;
      padding: 0px 15px;
      margin: 0 auto;
    }
    &__nav {
      max-width: 370px;
      width: 100%;
      &_list {
        display: flex;
        justify-content: space-between;
        max-width: 370px;
        width: 100%;
      }
    }
    &__text {
      font-size: 14px;
      font-weight: 400;
      line-height: 150%;
      color: #fff;
      opacity: 0.6;
    }
    &__text:hover {
        opacity: 1;
    }
  }
</style>