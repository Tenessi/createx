<template>
  <footer class="footer">
    <div class="footer__container">
      <div class="footer__column">
        <h6 class="footer__title">
          HELP
        </h6>
        <ul  class="footer__list">
          <li v-for="item in help_block" v-bind:key="item.id" class="footer__item">
            <a class="footer__link" :href="item.link">
              {{ item.name }}
            </a>
          </li>
        </ul>
      </div>
      <div class="footer__column">
        <h6 class="footer__title">
          SHOP
        </h6>
        <ul class="footer__list">
          <li v-for="item in shop_block" v-bind:key="item.id" class="footer__item">
            <a class="footer__link" :href="item.link">
              {{ item.name }}
            </a>
          </li>
        </ul>
      </div>
      <div class="footer__column">
        <h6 class="footer__title">
          GET IN TOUCH
        </h6>
        <div v-for="item in contacts_block" v-bind:key="item.id" class="footer__contacts_row">
          <span class="footer__contacts_title footer__link">{{ item.name }}</span>
          <a class="footer__link" :href="item.link">{{ item.link_name }}</a>
        </div>
        <div class="footer__network">
          <a v-for="item in social_network" v-bind:key="item.id" class="footer__network_link" :href="item.link">
            <img class="footer__network_image" :src="item.image" :alt="item.alt">
          </a>
        </div>
      </div>
      <div class="footer__column">
        <h6 class="footer__title">
          DOWNLOAD OUR APP
        </h6>
        <div class="footer__buttons">
          <a class="footer__buttons_link" v-for="item in download_block" v-bind:key="item.id" :href="item.link">
            <img class="footer__buttons_image" :src="item.image" :alt="item.alt">
          </a>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
  export default {
    data() {
      return {
        help_block: [
          {
            id: 'help_id_1',
            name: 'Delivery & returns',
            link: ''
          },
          {
            id: 'help_id_2',
            name: 'FAQ',
            link: ''
          },
          {
            id: 'help_id_3',
            name: 'Track order',
            link: ''
          },
          {
            id: 'help_id_4',
            name: 'Contacts',
            link: ''
          },
          {
            id: 'help_id_5',
            name: 'Blog',
            link: ''
          },
        ],
        shop_block: [
          {
            id: 'shop_id_1',
            name: 'New arrivals',
            link: ''
          },
          {
            id: 'shop_id_2',
            name: 'Trending now',
            link: ''
          },
          {
            id: 'shop_id_3',
            name: 'Sales',
            link: ''
          },
          {
            id: 'shop_id_4',
            name: 'Brands',
            link: ''
          },
        ],
        contacts_block: [
          {
            id: 'contacts_id_1',
            name: 'Call:',
            link_name: '(405) 555-01-28',
            link: ''
          },
          {
            id: 'contacts_id_2',
            name: 'Email:',
            link_name: 'hello@createx.com',
            link: ''
          }
        ],
        social_network: [
          {
            id: 'secial_network_1',
            image: '/images/footer/Facebook.svg',
            link: '',
            alt: 'Facebook button'
          },
          {
            id: 'secial_network_2',
            image: '/images/footer/Instagram.svg',
            link: '',
            alt: 'Instagram button'
          },
          {
            id: 'secial_network_3',
            image: '/images/footer/Twitter.svg',
            link: '',
            alt: 'Twitter button'
          },
          {
            id: 'secial_network_4',
            image: '/images/footer/Youtube.svg',
            link: '',
            alt: 'Youtube button'
          },
          {
            id: 'secial_network_5',
            image: '/images/footer/pinterest.svg',
            link: '',
            alt: 'Pinterest button'
          }
        ],
        download_block: [
          {
            id: 'download_id_1',
            image: '/images/footer/app-store.jpg',
            link: '',
            alt: 'App Store button'
          },
          {
            id: 'download_id_2',
            image: '/images/footer/google-play.jpg',
            link: '',
            alt: 'Google play button'
          },
        ]
          
        
      }
    }

  }

</script>

<style lang="scss">
  .footer {
    margin-top: 65px;
    background: #1E212C;
    &__container {
      display: flex;
      justify-content: space-between;
      max-width: 1260px;
      width: 100%;
      padding: 60px 15px 40px 15px;
      margin: 0 auto;   
    }
    &__title {
      margin-bottom: 12px;
      font-size: 16px;
      font-weight: 700;
      line-height: 160%;
      letter-spacing: 1px;
      color: #FFF;
    }
    &__item {
      margin-top: 4px;
    }
    &__link {
      font-size: 16px;
      font-weight: 400;
      line-height: 160%; 
      opacity: 0.6;
      color: #FFF;
    }
    &__link:hover {
      opacity: 1;
    }
    &__contacts {
      &_row {
        display: flex;
        margin-top: 4px;
      }
      &_title {
        margin-right: 4px;
        opacity: 1;
      }
    }
    &__buttons {
      display: flex;
      margin-top: 24px;
      &_link:not(:last-child) {
        margin-right: 20px;
      }
      &_image {
        border-radius: 8px;
      }
    }
    &__network {
      display: flex;
      &_link {
        margin-top: 24px;
        padding: 8px;
        border-radius: 4px;
        box-shadow: 0px 4px 4px 0px rgba(0, 0, 0, 0.25);
        background: #292929;
        transition: all 0.2s ease-in-out;
      }
      &_link:not(:last-child) {
        margin-right: 12px;
      }
      &_link:hover {
        margin-top: 20px;
      }
    }
  }
  
</style>