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
        >
        <div slot="tabOne">
            <codeGenerator
            :codeTitle="page.topBanner"
            :codeDescription="page.topBannerDescription"
            bannerClass="custom-banner"
            heading="h3"
        />
        </div>
        <div slot="tabTwo">
          <codeGenerator id="middleBanner" 
              :codeTitle="page.middleBanner"
              :codeDescription="page.middleBannerDescription"
              bannerClass="hp-middle-banner"
              heading="h2"
          />
        </div>
        <div slot="tabThree">
          <codeGenerator id="bottomBanner"
              :codeTitle="page.bottomBanner"
              :codeDescription="page.bottomBannerDescription"
              bannerClass="hp-bottom-banner"
              heading="h2"
          />
        </div>
        </tabs>
        <footerMessage
          snackBarMessage="Success"
        />
       <footerNavigation 
          :previousArticle="page.chapterThree"
          :nextArticle="page.introChapter"
          nextUrl="/"
          previousUrl="/banners"
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
    data:function () {
        return {
          isActive: true,
          middleActive: false,
          message: 'Hello there',
          Success: 'hi'
        }
    },
    methods: {
    onCopy: function (e) {
      alert('You just copied: ' + e.text)
    },
    onError: function (e) {
      alert('Failed to copy texts')
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