<template>
    <div class="burger-nav">
      <div class="close" >
          <p @click="isActive = !isActive" ><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-menu"><line x1="3" y1="12" x2="21" y2="12"></line><line x1="3" y1="6" x2="21" y2="6"></line><line x1="3" y1="18" x2="21" y2="18"></line></svg></p> 
        </div>
      <transition name="fade">
        <div class="container" :class="{ passive: isActive }">
              <div class="mobile-links">
                  <ul>
                      <li @click="isActive = !isActive">
                        <nuxt-link to="/">{{introContent}}</nuxt-link>
                      </li>
                      <li @click="isActive = !isActive">
                        <nuxt-link to="/images">{{contentOne}}</nuxt-link>
                      </li>
                      <li @click="isActive = !isActive">
                        <nuxt-link to="/banners">{{contentTwo}}</nuxt-link>
                      </li>
                      <li @click="isActive = !isActive">
                        <nuxt-link to="/carousel">{{contentThree}}</nuxt-link>
                      </li>
                      <li @click="isActive = !isActive">
                        <nuxt-link to="/social-media">{{contentFour}}</nuxt-link>
                      </li>
                      <li @click="isActive = !isActive">
                        <nuxt-link to="/amount">{{contentFive}}</nuxt-link>
                      </li>
                      <li @click="isActive = !isActive">
                        <nuxt-link to="/contact">{{contentSix}}</nuxt-link>
                      </li>
                      <li @click="isActive = !isActive">
                        <nuxt-link to="/contact">{{contentSeven}}</nuxt-link>
                      </li>
                  </ul>
              </div>
        </div> 
      </transition>
    </div>
</template>

<script>


export default {
    name: 'sideBar',
    data () {
      return {
        isActive: true
      }
    },
    props: [
        'contentOne', 
        'contentTwo', 
        'contentThree',
        'contentFour',
        'contentFive',
        'contentSix',
        'contentSeven',
        'introContent'
        ]
}
</script>



<style lang="scss">

.fade-enter-active, .fade-leave-active {
  transition: opacity .5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 1;
}

.passive {
  opacity: 1;
  z-index: -1000;
  height: 0vh;
  transform: translateX(100%) !important;
}

    .close {
      width: 100%;
      height: 100px;
      z-index: 10000;
      display: flex;
      justify-content: flex-end;
      align-items: center;
      position: fixed;
      p {
        padding: 24px;
        background-color: white;
        font-weight: bold;
      }
    }

.burger-nav {
  z-index: 1000;
  height: 100px;
  width: 100%;
  @media only screen and (min-width: 800px) {
    display: none;
  }
  .container {
    position: fixed;
    height: 100vh;
    top: 0;
    background-color: white;
    width: 100%;
    z-index: 1000;
    transition: .4s ease-in;
    transform: translateX(0px);
  }
}


.mobile-links {
  display: flex; 
  justify-content: flex-end;
  text-align: right;
  padding: 0;
  margin: 20vh 24px 0 0;
  ul {
    text-align: right;
    padding-left: 0;
    list-style-type: none;
    a {
      display: flex;
      text-align: right;
      justify-content: flex-end;
      text-decoration: none;
      opacity: .2;
      margin: 16px 0;
    }
  }
}


.nuxt-link-exact-active {
  opacity: 1 !important;
  color: $blue-color;
  font-weight: 600;
}


@media only screen and (max-width: 720px) {
    .burger-nav {
        display: block;
    }
}

</style>
