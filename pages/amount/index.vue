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
        />
      </aside>
    <div class="col2">
      <nuxt-content :document="page"></nuxt-content>
      <div class="container">
        <!-- VELIKOSTI OBRÁZKŮ -->
        <imageTutorial id="images"
          :sectionTitle="page.chapterSeven"
          :sectionDescription="seven.description"
          tutorialImage="https://alexborecky.com/images/shoptet/amount.png">
        </imageTutorial>
        <additionalContent>
          <div slot="additionalContent">
            <snackBar class="warning no-link"
              :snackBarText="seven.warning"
              snackBarLink="Přejít na generátor"
              snackUrl=""
            />
            <step class="step-one step-no-image"
                :stepTitle="seven.stepOne"
                :stepText="seven.oneText"
                stepImage=""
                >
                <div slot="stepContent">
                    <pre class="snippet">
                        <code>
                            <div class="wrapper">
                                <strong class="red"> {{seven.snippetOne}} </strong>
                            </div>
                        </code>
                    </pre>
                </div>
              </step>
              <step class="step-two step-no-image"
                :stepTitle="seven.stepTwo"
                :stepText="seven.twoText"
                stepImage=""
                >
                <div slot="stepContent">
                  <pre>
                    <code>
                      <div class="wrapper">
                        <div class="first-layer">
                          <span>&lt;</span><span class="red">style</span><span>></span>
                        </div>
                          <div class="second-layer">
                            <span class="css-orange">.type-detail .product-top .add-to-cart .quantity </span> {
                          </div>
                            <div class="third-layer">
                              <span class="css-green">display</span>: <span class="css-yellow">none</span>;
                            </div>
                          <div class="second-layer">
                            }
                          </div>
                        <div class="first-layer">
                          <span>&lt;</span>/<span class="red">style</span><span>></span>
                        </div>
                      </div>
                    </code>
                  </pre>
                </div>
              </step>
          </div>
        </additionalContent>
        <footerNavigation 
          :previousArticle="page.chapterFive"
          :nextArticle="page.chapterSix"
          nextUrl="/generator"
          previousUrl="/logos"
        />
      </div>
    </div>
  </div>
</template>
 
<script>
 
export default {
  async asyncData({$content}) {
    const page = await $content('home').fetch();
    const seven = await $content('chapterSeven').fetch();
    return { page, seven }
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

<style lang="scss" scoped>

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

.step-two {
  img {
    display: none;
  }
}

.codepen {
  margin: 24px 0 0 0;
}

.image-slot {
  background-size: 100% auto !important;
  background-repeat: no-repeat;
  height: 240px !important;
}

</style>
