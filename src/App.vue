<script>
import MainHeader from './components/MainHeader.vue';
import MainFooter from './components/MainFooter.vue';

// // icone
import digitalComicsIcon from './assets/img/digital-comics.png';
import merchandiseIcon from './assets/img/merchandiseIcon.png';
import subscriptionIcon from './assets/img/subscriptionIcon.png';
import comicShopLocatorIcon from './assets/img/comic-shop-locator.png';
import dcPowerVisaIcon from './assets/img/dc-power-visa.svg';


export default{
  name: 'app',
  components: {
    MainHeader,
    MainFooter
  },
  data() {
    return {
      infoItems: [
        { icon: digitalComicsIcon, text: 'DIGITAL dsadasdas COMICS', alt: 'Digital Comics' },
        { icon: merchandiseIcon, text: 'DC MERCHANDISE', alt: 'DC Merchandise' },
        { icon: subscriptionIcon, text: 'SUBSCRIPTION', alt: 'Subscription' },
        { icon: comicShopLocatorIcon, text: 'COMIC SHOP LOCATOR', alt: 'Comic Shop Locator' },
        { icon: dcPowerVisaIcon, text: 'DC POWER VISA', alt: 'DC Power Visa' },
      ]
    };
  }
};
</script>




<template>
  <div>

    <MainHeader />

    <main>
      <div class="content">
        <!-- Content goes here -->
      </div>
      <div class="info-bar">
        <div class="info-item" v-for="(item, index) in infoItems" :key="index">
          <img :src="item.icon" :alt="item.alt" />
          <span>{{ item.text }}</span>
        </div>
      </div>
    </main>

    <MainFooter />

  </div>
</template>





<style lang="scss" src="./style.css">
  /* regole SCSS */
</style>
