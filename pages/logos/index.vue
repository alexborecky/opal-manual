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
          :sectionTitle="page.chapterFive"
          :sectionDescription="five.description"
          tutorialImage="https://alexborecky.com/images/shoptet/logos.png">
        </imageTutorial>
        <div class="additional-content">
            <step class="step-one step-no-image"
                :stepTitle="five.stepOne"
                :stepText="five.oneText"
                stepImage=""
                >
                <div slot="stepContent">
                    <pre class="snippet">
                        <code>
                            <div class="wrapper">
                                <strong class="red"> {{five.snippetOne}} </strong>
                            </div>
                        </code>
                    </pre>
                </div>
              </step>
              <step class="step-two"
                :stepTitle="five.stepTwo"
                :stepText="five.twoText"
                stepImage="https://alexborecky.com/images/shoptet/logos-image.png"
                >
              </step>
              <step class="step-three step-no-image"
                :stepTitle="five.stepThree"
                :stepText="five.threeText"
                stepImage=""
                >
                <div slot="stepContent">
                  <pre>
                    <code>
                      <div class="wrapper">
                        <div class="first-layer">
                          <span>&lt;</span><span class="red">div</span><span>></span>
                        </div>
                            <div class="second-layer">
                                &lt;<span class="red">img</span> <span class="yellow">src</span>="<span class="green">{{visaImg}}</span>"> 
                            </div>
                            <div class="second-layer">
                                &lt;<span class="red">img</span> <span class="yellow">src</span>="<span class="green">{{masterImg}}</span>"> 
                            </div>
                            <div class="second-layer">
                                &lt;<span class="red">img</span> <span class="yellow">src</span>="<span class="green">{{paypalImg}}</span>"> 
                            </div>
                        <div class="first-layer">
                          <span>&lt;</span>/<span class="red">div</span><span>></span>
                        </div>
                      </div>
                    </code>
                  </pre>
                </div>
              </step>
              <step class="step-four"
                :stepTitle="five.stepFour"
                :stepText="five.fourText"
                stepImage="https://alexborecky.com/images/shoptet/logos-settings.png"
                >
              </step>
        </div>
        <footerNavigation 
          :previousArticle="page.chapterFour"
          :nextArticle="page.chapterSeven"
          nextUrl="/amount"
          previousUrl="/social-media"
        />
      </div>
    </div>
  </div>
</template>
 
<script>
 
export default {
  async asyncData({$content}) {
    const page = await $content('home').fetch();
    const five = await $content('chapterFive').fetch();
    return { page, five }
  },
  name: 'app',
  components: {
  },
  data () {
    return {
      some: 'Hello',
      visaImg: 'https://cdn.myshoptet.com/usr/shoptet.tomashlad.eu/user/documents/extras/opal/img/payments/visa.svg',
      masterImg: 'https://cdn.myshoptet.com/usr/shoptet.tomashlad.eu/user/documents/extras/opal/img/payments/mastercard.svg',
      paypalImg: 'https://cdn.myshoptet.com/usr/shoptet.tomashlad.eu/user/documents/extras/opal/img/payments/paypal.svg'
    }
  }
}
</script>

<style lang="scss" scoped>

.step-one, .step-three {
    img {
        display: none;
    }
}

</style>
