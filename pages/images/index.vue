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
      <nuxt-content :document="page"></nuxt-content>
      <div class="container">
        <!-- VELIKOSTI OBRÁZKŮ -->
        <imageTutorial id="images"
          :sectionTitle="page.chapterOne"
          :sectionDescription="page.chapterOneDescription"
          tutorialImage="https://alexborecky.com/images/shoptet/imageSize.png">
          <div slot="additionalContent">
            <p>{{page.chapterOneAdditionOne}}</p>
            <div class="additional-image"></div>
            <snackBar class="no-link warning"
              :snackBarText="page.imageSizeText"
              snackBarLink=""
              snackUrl=""
            />
          </div>
        </imageTutorial>
        <footerNavigation 
          :previousArticle="page.introChapter"
          :nextArticle="page.chapterTwo"
          nextUrl="/banners"
          previousUrl="/"
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
  components: {
  },
  data () {
    return {
      some: 'Hello'
    }
  }
}
</script>

<style lang="scss">

.back-button {
  position: relative;
  top: 40px !important;
    .underline {
    height: 2px;
    width: 100%;
    background-color: black;
    position: absolute;
  }
}

.additional-content img {
  width: 100%;
  margin-top: 24px;
}

.additional-image {
  margin: 24px 0 0 0 ;
  display: none;
}

#banners {  
  .step-two, .step-three {
    p:nth-child(4){
      display: none;
    }
}

}

.codepen {
  margin: 24px 0 0 0;
}

</style>
