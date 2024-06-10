<script>
import MainHeader from './components/MainHeader.vue';
import MainFooter from './components/MainFooter.vue';


export default{
  name: 'app',
  components: {
    Header,
    Footer
  },
  data() {
    return {
      infoItems: [
        { icon: '/src/assets/img/digital-comics.png', text: 'DIGITAL COMICS', alt: 'Digital Comics' },
        { icon: '/src/assets/img/merchandise.png', text: 'DC MERCHANDISE', alt: 'DC Merchandise' },
        { icon: '/src/assets/img/subscription.png', text: 'SUBSCRIPTION', alt: 'Subscription' },
        { icon: '/src/assets/img/comic-shop-locator.png', text: 'COMIC SHOP LOCATOR', alt: 'Comic Shop Locator' },
        { icon: '/src/assets/img/dc-power-visa.png', text: 'DC POWER VISA', alt: 'DC Power Visa' },
      ]
    };
  }
};
</script>




<template>
 
  <Mainheader />


  <main>
      <div class="content">
        <!-- Content here -->
      </div>
      <div class="info-bar">
        <div class="info-item" v-for="(item, index) in infoItems" :key="index">
          <img :src="item.icon" :alt="item.alt" />
          <span>{{ item.text }}</span>
        </div>
      </div>
  </main>


  <MainFooter />

</template>





<style lang="scss" src="./style.css">
  /* regole SCSS */
</style>
