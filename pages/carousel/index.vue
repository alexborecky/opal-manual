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
        <!-- NASTAVENI CAROUSELU -->
        <videoTutorial id="carousel"
          :sectionTitle="page.chapterThree"
          :sectionDescription="page.chapterThreeDescription">
          <div slot="codepen">
            <p>Než začneme s konkrétními kroky, podívejme se na kód, který budeme do administrace zadávat.</p>
            <codeSnippet
              :bannerClass="codes.carouselClass"
              :imageUrl="codes.carouselImage"
              :bannerClassTwo="codes.carouselSecondClass"
              :heading="codes.carouselTypo"
              :title="codes.carouselTitle"
              :description="codes.carouselDescription"
              :buttonUrl="codes.carouselButton"
              :buttonText="codes.carouselButtonText"
            />
            <!-- <iframe 
              height="320" 
              style="width: 100%; border: none"  
              src="https://codepen.io/alexborecky/embed/eYZgjGb?height=231&theme-id=dark&default-tab=html">
            </iframe> -->
          </div> 
          <div class="video-slot" slot="youtube">
            <iframe 
              width="100%" 
              height="100%" 
              src="https://www.youtube.com/embed/qhgvgkP6yzA"
              frameborder="0" 
              allow="accelerometer; 
              autoplay; 
              encrypted-media; 
              gyroscope; 
              picture-in-picture" 
              allowfullscreen>
            </iframe>
          </div>
        </videoTutorial>
        <additionalContent>
            <div slot="additionalContent">
              <step class="step-one"
                    :stepTitle="page.stepOneCarousel"
                    :stepText="page.stepOneTextCarousel"
                    :stepTextTwo="page.stepOneTextTwoCarousel"
                    stepImage="https://alexborecky.com/images/shoptet/carousel-main.png">

                    <div slot="stepContent">
                      <snackBar class="no-link warning"
                        :snackBarText="page.carouselWarning"
                        snackBarLink=""
                        snackUrl=""
                      />
                      <p>Hotovo? Výborně 👍! Jdeme dál</p>
                    </div>

              </step>

              <!-- STEP TWO -->
              <step class="step-two"
                  :stepTitle="page.stepTwo"
                  :stepText="page.stepTwoText"
                  :stepTextTwo="page.stepTwoTextTwo"
                  stepImage="https://alexborecky.com/images/shoptet/carousel-image.png">

                  <!-- ADDITIONAL STEP TWO CONTENT -->
                  <div slot="stepContent">

                    <p>
                      Podívejme se znovu na náš kód, který budeme vkládat do administrace Shoptetu.
                    </p>
                    <codeSnippet
                      :bannerClass="codes.carouselClass"
                      :imageUrl="codes.carouselImage"
                      :bannerClassTwo="codes.carouselSecondClass"
                      :heading="codes.carouselTypo"
                      :title="codes.carouselTitle"
                      :description="codes.carouselDescription"
                      :buttonUrl="codes.carouselButton"
                      :buttonText="codes.carouselButtonText"
                    />

                    <!-- <iframe class="codepen"
                      height="320" 
                      style="width: 100%; border: none"  
                      src="https://codepen.io/alexborecky/embed/eYZgjGb?height=231&theme-id=dark&default-tab=html">
                    </iframe> -->

                    <p> 
                      V první v řadě změníme obsah za textem <span class="orange"> src </span> v <span class="yellow"><span class="yellow">&lt;</span>img&gt;</span> atributu a mezi uvozovkami, který reprezentuje obrázek, jenž je v pozadí banneru.
                    </p>

                    <pre slot="additionalContent" class="wrap-code">
                      <code> 
                        <div class="wrapper green"> https://cdn.myshoptet.com/usr/shoptet.tomashlad.eu/user/documents/extras/opal/img/slide1.png?v5
                        </div>
                      </code>
                    </pre>

                    <p>
                      Tento kód je třeba nahradit adresou obrázku, který chete na místě mít. Tuto adresu získáte buď přepsáním z vašeho FTP, nebo kliknutím pravým tlačítkem na obrázek na webu a zkopírováním adresy obrázku.
                    </p>
                  </div>

              </step>

              <!-- STEP THREE    -->
              <step class="step-three"
                  :stepTitle="page.stepThree"
                  :stepText="page.stepThreeText"
                  :stepTextThree="page.stepThreeTextTwo"
                  stepImage="https://alexborecky.com/images/shoptet/carousel-text.png">

                  <div slot="stepContent">
                    <p> Nahrazení textu je snažší, neboť se můžeme orientovat podle již zkopírovaného textu, konkrétně 
                      <span class="red"> Nahradíme nadpisem banneru </span> a 
                      <span class="red"> Nahradíme popiskem hlavního banneru </span> v attrbitutech 
                      <code>
                        &lt;<span class="red">h2</span>>
                      </code> a 
                      <code>
                        &lt;<span class="red">p</span>&gt;
                      </code>
                    </p> 
                    
                    <pre slot="additionalContent">
                      <code> 
                        <div class="wrapper">
                          &lt;<span class="red">h2</span>&gt;<span class="white">Nahradíme nadpisem banneru</span>&lt;/<span class="red">h2</span>&gt;<br>
                          &lt;<span class="red">p</span>&gt;<span class="white">Nahradíme popiskem hlavního banneru</span>&lt;/<span class="red">p</span>&gt;
                        </div>
                      </code>
                    </pre> 

                    <p>
                      Tento text můžete nahradit libovolným textem, který sedí konrétnímu banneru. Doporučujeme neprodlužovat délku nadpisu, neboť je pro uživatele přitažlivější krátký a jasný text, než dlouhé nadpisy.
                    </p>
                  </div>
              </step>

              <!-- STEP FOUR -->
              <step class="step-four"
                :stepTitle="page.stepFour"
                  :stepText="page.stepFourText"
                  :stepTextFour="page.stepFourTextTwo"
                  stepImage="https://alexborecky.com/images/shoptet/carousel-text.png">

                  <div slot="stepContent">
                    <p> Podíváme se na zoubek obsahu mezi uvozovkami 
                      <code><span class="orange">href</span></code> v atribtutu <code>
                      &lt;<span class="red">a</span>></code>
                      který reprezentuje link / adresu, kam bude tlačítko směřovat. V tuto chvíli máme na tomto místě pouze vyplněný hashtag #.
                    </p>

                    <pre slot="additionalContent">
                      <code>
                        <div class="wrapper">
                          <span class="yellow">href</span>="<span class="green">#</span>"
                        </div>
                      </code>
                    </pre> 

                    <p>
                      Tento hashtag nahradíme adresou, na kterou chceme aby tlačítko banneru směřovalo. Pokud směřuje na slevu, či prodkut na vašem e-shopu, pak stačí nahradit # adresou konkrétní stranky produktu, či jiné.
                    </p>
                    
                    <p>
                      Druhá část je text, který definuje text tlačítka v banneru. V našem případě je to nyní 
                      <span class="red">Kliknutí na odkaz</span>
                    </p>

                    <pre>
                      <code>
                        <div class="wrapper">
                          &lt;<span class="red">a</span> <span class="yellow">href</span>="<span class="green">#</span>" <span class="yellow">class</span>="<span class="green">button</span>"><span class="white">Kliknutí na odkaz</span>&lt;/<span class="red">a</span>>
                        </div>
                        </code>
                    </pre>

                    <p>
                      Nahradíme-li tento text jakýmkoliv, který bude příznačný pro konkrétní tlačítko, změna se nám projeví.
                    </p>
                  </div>

              </step>
            </div>
        </additionalContent>
          <snackBar class="success"
            :snackBarText="generatorTip"
            snackBarLink="Přejít na generátor"
            snackUrl="/generator"
          />
            <footerNavigation 
            :previousArticle="page.chapterTwo"
            :nextArticle="page.chapterFour"
            nextUrl="/social-media"
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
    const codes = await $content('codes').fetch();
    return {page, codes}
  },
  name: 'app',
  components: {
  },
  data () {
    return {
      name1: 'sectionTitle',
      chapterFour: 'sectionTitle',
      generatorTip: 'TIP! Vyzkoušejte náš generátor kódu pro bannery! Stačí vyplnit obsahová pole a kód máte pžipravený pro použiti.',
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

.wrap-code {
    white-space: nowrap;
    overflow: auto;
    code {
      margin: 24px;
      .wrapper {
        margin-left: 24px;
      }
    }
}

</style>
