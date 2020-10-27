<template>
  <div class="hero home-page">
    <div class="home-container">
      <div class="heading">
        <div class="logo">
          <img src="@/assets/images/manualy-logo.svg" alt="">
        </div>
        <h2>Dokumentace</h2>
        <p>Vítejte v dokumentační aplikaci doplňků Shopteťák.cz!</p>
      </div>
      <div class="dashboard">
        <div class="recent dashboard-section">
          <div class="title flex">
            <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M12 6V12L16 14M22 12C22 17.5228 17.5228 22 12 22C6.47715 22 2 17.5228 2 12C2 6.47715 6.47715 2 12 2C17.5228 2 22 6.47715 22 12Z" stroke="#1E1E1C" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"/>
            </svg>
            <h4>Nejnovější doplňky</h4>
          </div>
          <div class="row">
            <templateCard
              tempTitle="Opal"
              tempDes="Minimalistická Blank šablona zaměřující se na obsah"
              tempLink="/opal"
            />
            <addonCard class="see-badge preparing"
              addonTitle="Premium Carousel"
              addonDes="Interaktivní vylepšení všedního Shoptet Carouselu"
              addonLink="/premiumCarousel"
            />
            <templateCard class="see-badge preparing"
              tempTitle="Celestin"
              tempDes="Interaktivní vylepšení všedního Shoptet Carouselu"
              tempLink="/celestin"
            />
          </div>
        </div>
        <div class="templates dashboard-section">
          <div class="title flex">
            <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M3 9H21M9 21V9M5 3H19C20.1046 3 21 3.89543 21 5V19C21 20.1046 20.1046 21 19 21H5C3.89543 21 3 20.1046 3 19V5C3 3.89543 3.89543 3 5 3Z" stroke="#1E1E1C" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
            </svg>
            <h4>Šablony</h4>
          </div>
          <div class="row">
            <templateCard
              tempTitle="Opal"
              tempDes="Minimalistická Blank šablona zaměřující se na obsah"
              tempLink="/opal"
            />
            <templateCard class="see-badge preparing"
              tempTitle="Celestin"
              tempDes="Interaktivní vylepšení všedního Shoptet Carouselu"
              tempLink="/celestin"
            />
          </div>
        </div>
        <div class="addons dashboard-section">
          <div class="title flex">
            <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M12 8V16M8 12H16M5 3H19C20.1046 3 21 3.89543 21 5V19C21 20.1046 20.1046 21 19 21H5C3.89543 21 3 20.1046 3 19V5C3 3.89543 3.89543 3 5 3Z" stroke="#1E1E1C" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
            </svg>
            <h4>Doplňky</h4>
          </div>
          <div class="row">
            <addonCard class="see-badge preparing"
              addonTitle="Premium Carousel"
              addonDes="Interaktivní vylepšení všedního Shoptet Carouselu"
              addonLink="/premiumCarousel"
            />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
 
<script>
 
export default {
  async asyncData({$content}) {
    const page = await $content('home').fetch();
    return {page}
  },
  name: 'generator',
  components: {
  },
  data () {
    return {
      name1: 'sectionTitle',
      chapterFour: 'sectionTitle'
    }
  }
}
</script>

<style lang="scss" scoped>

.heading {
  .logo {
    margin-bottom: 40px;
  }
}

</style>
