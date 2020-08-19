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
        <codeGenerator 
            :codeTitle="page.topBanner"
            :codeDescription="page.topBannerDescription"
            bannerClass="custom-banner"
            heading="h3"
        />
        <codeGenerator 
            :codeTitle="page.middleBanner"
            :codeDescription="page.middleBannerDescription"
            bannerClass="hp-middle-banner"
            heading="h2"
        />
        <codeGenerator 
            :codeTitle="page.bottomBanner"
            :codeDescription="page.bottomBannerDescription"
            bannerClass="hp-bottom-banner"
            heading="h2"
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
    name: 'generator',
    data () {
        return {
        }
    }
}
</script>


<style lang="scss" scoped>
    
input {
    width: 600px;
}

.image-tutorial {

}

</style>