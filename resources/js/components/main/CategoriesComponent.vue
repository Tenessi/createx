<template>
  <div class="categories">
    <div v-for="block in blocks" v-bind:key="block.id" class="categories__block">
      <img class="categories__block_image" :src="block.img" alt="Background image">
      <h4 class="categories__block_title">{{ block.title }}</h4>
    </div>
  </div>
</template>

<script>

  export default {
    data() {
      return {
        blocks: [
          {
            id: 'categories_block_1',
            title: 'Women',
            img: 'images/main/categories/women.jpg'
          },
          {
            id: 'categories_block_2',
            title: 'Mens',
            img: 'images/main/categories/men.jpg'
          },
          {
            id: 'categories_block_3',
            title: 'Kids',
            img: 'images/main/categories/kids.jpg'
          }
        ]
      }
    },

  }

</script>

<style lang="scss">
  .categories {
    display: flex;
    max-width: 1260px;
    width: 100%;
    padding: 0px 15px;
    margin: 0 auto;
    &__block {
      display: flex;
      flex-direction: column;
      transition: all 0.3s ease-in-out;
      cursor: pointer;
      &_image {
        max-width: 390px;
        width: 100%;
        max-height: 390px;
        height: 100%;
        border-radius: 4px;
      }
      &_title {
        margin-top: 16px;
        text-align: center;
        font-size: 20px;
        font-weight: 700;
        line-height: 150%;
        color: #424551;
      }
    }
    &__block:not(:last-child) {
      margin-right: 30px;
    }
    &__block:hover {
      margin-top: -30px;
    }
  }
</style>