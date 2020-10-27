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
      <div class="container">
        <nuxt-content :document="page"></nuxt-content>
        <textTutorial
          :sectionTitle="page.chapterFour"
          :sectionDescription="chapterFour.description"
          :sectionDescriptionThree="page.chapterFourDescriptionThree"
          >
        </textTutorial>
        <additionalContent>
            <div slot="additionalContent">
              <step class="step-one step-no-image"
                :stepTitle="chapterFour.stepOne"
                :stepText="chapterFour.oneText"
                stepImage=""
                >
                <div slot="stepContent">
                    <pre class="snippet">
                        <code>
                            <div class="wrapper">
                                <strong class="red"> {{chapterFour.snippetOne}} </strong>
                            </div>
                        </code>
                    </pre>
                </div>
              </step>

              <!-- STEP TWO -->
              <step class="step-two"
                  :stepTitle="chapterFour.stepTwo"
                  :stepText="chapterFour.twoText"
                  stepImage="https://alexborecky.com/images/shoptet/contact.png">

                  <!-- ADDITIONAL STEP TWO CONTENT -->
                  <div slot="stepContent">
                    <snackBar class="no-link alert"
                        :snackBarText="chapterFour.alert"
                        snackBarLink="Přejít na generátor"
                        snackUrl=""
                    />
                  </div>
              </step>

              <!-- STEP THREE    -->
              <step class="step-three"
                  :stepTitle="chapterFour.stepThree"
                  :stepText="chapterFour.threeText"
                  stepImage="https://alexborecky.com/images/shoptet/social-media.png">

                  <!-- ADDITIONAL STEP Three CONTENT -->
                  <div slot="stepContent">
                    <p>{{chapterFour.threeTextAdd}}</p>
                    <div slot="stepContent">
                        <pre>
                            <code>
                                <div class="wrapper">
                                    <strong class="green"> {{chapterFour.snippetTwo}} </strong>
                                </div>
                            </code>
                        </pre>
                    </div>
                  </div>
              </step>

              <!-- STEP FOUR -->
              <step class="step-four"
                :stepTitle="chapterFour.stepFour"
                  :stepText="chapterFour.fourText"
                  stepImage="https://alexborecky.com/images/shoptet/social-footer.png">
                  <div slot="stepContent">
                  </div>
              </step>
            </div>
        </additionalContent>
          <snackBar class="warning no-link"
            :snackBarText="chapterFour.snackTwo"
            snackBarLink="Přejít na generátor"
            snackUrl="/opal/generator"
          />
            <footerNavigation 
            :previousArticle="page.chapterThree"
            :nextArticle="page.chapterSix"
            nextUrl="/opal/generator"
            previousUrl="/opal/carousel"
            />
      </div>
    </div>
  </div>
</template>
 
<script>
 
export default {
  async asyncData({$content}) {
    const page = await $content('home').fetch();
    const chapterFour = await $content('chapterFour').fetch();
    return { page, chapterFour }
  },
  name: 'app',
  components: {
  },
  data () {
    return {
      name1: 'sectionTitle',
      chapterFour: 'sectionTitle',
      generatorTip: 'TIP! Vyzkoušejte náš generátor kódu pro bannery! Stačí vyplnit obsahová pole a kód máte pžipravený pro použiti.'
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
