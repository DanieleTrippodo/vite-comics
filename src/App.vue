<script>
import MainHeader from './components/MainHeader.vue';
import MainFooter from './components/MainFooter.vue';
import ComicList from './components/ComicList.vue';

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
    MainFooter,
    ComicList
  },
  data() {
    return {
      infoItems: [
        { icon: digitalComicsIcon, text: 'DIGITAL COMICS', alt: 'Digital Comics' },
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

    <!-- -Header -->
    <MainHeader />
    <!-- -Header -->



    <!-- -Main--------------------------------------------------------------------------- -->
    <main>


      <!-- todo - Aggiungere il Jumbotron - Da cambiare -->
      <img src="./assets/img/jumbotron.jpg" alt="PlaceHolder" id="Jumbotron">


      <!-- sezione 'Current Series' -->
      <ComicList />

    </main>
    <!-- -Main -------------------------------------------------------------------------- -->



    <!-- -Footer -->
    <MainFooter />
    <!-- -Footer -->
  </div>
</template>





<style lang="scss" src="./style.css">
  /* regole SCSS */
  @import './styles/main.scss';
</style>
