<!-- Qui va la logica del componente (Vue3 + Javascript) -->
<script>
export default {
  name: 'MainFooter',
  data() {
    return {
      infoItems: [
        { icon: '/src/assets/img/digital-comics.png', text: 'DIGITAL COMICS', alt: 'Digital Comics' },
        { icon: '/src/assets/img/merchandiseIcon.png', text: 'DC MERCHANDISE', alt: 'DC Merchandise' },
        { icon: '/src/assets/img/subscriptionIcon.png', text: 'SUBSCRIPTION', alt: 'Subscription' },
        { icon: '/src/assets/img/comic-shop-locator.png', text: 'COMIC SHOP LOCATOR', alt: 'Comic Shop Locator' },
        { icon: '/src/assets/img/dc-power-visa.svg', text: 'DC POWER VISA', alt: 'DC Power Visa' },
      ],
      footerSections: [
        {
          title: 'DC COMICS',
          items: ['Characters', 'Comics', 'Movies', 'TV', 'Games', 'Videos', 'News']
        },
        {
          title: 'DC',
          items: ['Terms Of Use', 'Privacy policy (New)', 'Ad Choices', 'Advertising', 'Jobs', 'Subscriptions', 'Talent Workshops', 'CPSC Certificates', 'Ratings', 'Shop Help', 'Contact Us']
        },
        {
          title: 'SITES',
          items: ['DC', 'MAD Magazine', 'DC Kids', 'DC Universe', 'DC Power Visa']
        },
        {
          title: 'SHOP',
          items: ['Shop DC', 'Shop DC Collectibles']
        }
      ]
    };
  }
};
</script>



<!-- Qui va il contenuto di questo elemento (HTML) -->
<template>
  <footer>


    <div class="info-bar">
      <div class="info-item" v-for="(item, index) in infoItems" :key="index">
        <img :src="item.icon" :alt="item.alt" />
        <span>{{ item.text }}</span>
      </div>
    </div>


    <div class="footer-content">
      <div class="footer-section" v-for="(section, index) in footerSections" :key="index">
        <h4>{{ section.title }}</h4>
        <ul>
          <li v-for="(item, idx) in section.items" :key="idx">{{ item }}</li>
        </ul>
      </div>
    </div>


    <div class="signup flex-follow">
      <button>SIGN-UP NOW!</button>


      <div class="social-media">
        <span>FOLLOW US</span>
        <!-- Add social media icons here -->
      </div>


    </div>



  </footer>
</template>



<!-- Qui va lo stile CSS di questo elemento (CSS) -->
<style scoped lang="scss">
footer {
  background-color: #333;
  color: #fff;
  padding-top: 0;

  /* for fixing the white space on the footer!   :o */
  margin-bottom: 0px;
  padding-bottom: 2.1rem;
  /* for fixing the white space on the footer!   :o */

  background-image: url('../assets/img/footer-bg.jpg');
  background-size: cover; 
  background-repeat: no-repeat;
  background-position: center; 

  .info-bar {
    background-color: #007bff;
    color: #fff;
    display: flex;
    justify-content: space-around;
    padding: 1rem 0;
    margin-bottom: 2rem;

    .info-item {
      display: flex;
      align-items: center;
      gap: 10px;

      img {
        height: 50px;
      }
    }
  }

  .footer-content {
    display: flex;
    justify-content: space-around;
  }

  .footer-section {
    h4 {
      margin-bottom: 10px;
    }

    ul {
      list-style: none;
      padding: 0;

      li {
        margin-bottom: 5px;
      }
    }
  }

  .signup {
    text-align: center;
    margin: 20px 0;

    button {
      background-color: #007bff;
      color: #fff;
      padding: 10px 20px;
      border: none;
      cursor: pointer;
    }
  }

  .social-media {
    text-align: center;

    span {
      display: block;
      margin-bottom: 10px;
    }

    /* Add styles for social media icons here */
  }
}


.flex-follow{
  display: flex;
  justify-content: flex-start;
  align-items: baseline;

  gap: 5rem;
  margin-left: 1rem;
  padding-left: 5rem;
  padding-top: 3rem;
}
</style>