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
          :contentSeven="page.chapterSeven"
          :contentEight="page.chapterEight"
          :contentNine="page.chapterNine"
          :contentTen="page.chapterTen"
        />
      </aside>
    <div class="col2">
      <div class="container home-page">
        <intro
          :templateTitle="page.templateTitle"
          :introDescription="page.introDescription"
          :introSubtitle="page.introSubtitle"
          :introSubtextOne="page.introSubtextOne"
          :introSubtextTwo="page.introSubtextTwo"

          introSnackLink=""
          :introSnackBar="page.snackBarWarning"
          introSnackUrl=""
        />
        <nuxt-content :document="page"></nuxt-content>
        <footerNavigation 
          :previousArticle="page.introChapter"
          :nextArticle="page.chapterOne"
          nextUrl="/images"
          previousUrl=""
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

<style lang="scss">

.home-page {
  .footer-navigation {
    a:nth-child(1) {
      visibility: hidden !important;
    }
  }
}

</style>
