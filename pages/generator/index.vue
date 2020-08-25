<template>
  <div class="flex-row-hero">
    <aside class="col1">
      <contentList id="content-list"
          :introContent="page.introChapter"
          :contentOne="page.chapterOne"
          :contentTwo="page.chapterTwo"
          :contentThree="page.chapterThree"
          :contentFour="page.chapterFour"
          :contentFive="page.chapterFive"
          :contentSix="page.chapterSix"
        />
      </aside>
    <div class="col2">
      <div class="container flex column">
        <nuxt-content :document="page"></nuxt-content>
        <textTutorial
            :sectionTitle="page.chapterSix"
            :sectionDescription="page.chapterSixDescription"
        />
        <tabs
          :tabOneTitle="page.topBanner"
          :tabTwoTitle="page.middleBanner"
          :tabThreeTitle="page.bottomBanner"
          :tabFourTitle="page.carousel"
        >
        <div slot="tabOne">
            <codeGenerator
            :codeTitle="page.topBanner"
            :codeDescription="page.topBannerDescription"
            bannerType="Kód pro vrchní banner"
            bannerClass="custom-banner"
            heading="h3"
            bannerClassTwo="banner-caption"
        />
        </div>
        <div slot="tabTwo">
          <codeGenerator id="middleBanner" 
              :codeTitle="page.middleBanner"
              :codeDescription="page.middleBannerDescription"
              bannerType="Kód pro střední banner"
              bannerClass="hp-middle-banner"
              heading="h2"
              bannerClassTwo="banner-caption"
          />
        </div>
        <div slot="tabThree">
          <codeGenerator id="bottomBanner"
              :codeTitle="page.bottomBanner"
              :codeDescription="page.bottomBannerDescription"
              bannerType="Kód pro spodní banner"
              bannerClass="hp-bottom-banner"
              heading="h2"
              bannerClassTwo="banner-caption"
          />
        </div>
        <div slot="tabFour">
          <codeGenerator id="bottomBanner"
              :codeTitle="page.carousel"
              :codeDescription="page.carouselDescription"
              bannerType="Kód pro Carousel"
              bannerClass="carousel-slide-box"
              heading="h2"
              bannerClassTwo="carousel-slide-caption"
          />
        </div>
        </tabs>
        <footerNavigation 
          :previousArticle="page.chapterThree"
          :nextArticle="page.introChapter"
          nextUrl="/"
          previousUrl="/carousel"
        />
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
    name: 'app',
    data () {
        return {
          isActive: true,
          middleActive: false
        }
    }
}
</script>


<style lang="scss" scoped>


.passive {
  display: none;
}

.top, .middle, .bottom {
  display: none;
}
    
input {
    width: 600px;
}


.switchers {
  justify-content: space-between;
  .switcher {
    width: 24px;
  }
}

#middleBanner {
  z-index: 1000;
}

</style>