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
      <div class="container">
        <nuxt-content :document="page"></nuxt-content>
        <videoTutorial
          :sectionTitle="page.chapterTwo"
          :sectionDescription="page.chapterTwoDescription"
          :sectionDescriptionTwo="page.chapterTwoDescriptionTwo"
          :sectionDescriptionThree="page.chapterTwoDescriptionThree"
          >
          <!-- TOP CODEPEN -->
          <div slot="codepen">
            <iframe class="codepen"
              height="320" 
              style="width: 100%; border: none"  
              src="https://codepen.io/alexborecky/embed/xxVOyQb?height=231&theme-id=dark&default-tab=html">
            </iframe>
          </div>
          <!-- STEP FOUR -->
          <div class="video-slot" slot="youtube">
            <iframe 
              width="100%" 
              height="100%" 
              src="https://www.youtube.com/embed/d-LtMpDw9B0" 
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
                    :stepTitle="page.stepOne"
                    :stepText="page.stepOneText"
                    :stepTextTwo="page.stepOneTextTwo"
                    stepImage="https://alexborecky.com/images/admin-banner.png">

                    <div slot="stepContent">
                      <p>Hotovo? Výborně 👍! Jdeme dál</p>
                    </div>

              </step>

              <!-- STEP TWO -->
              <step class="step-two"
                  :stepTitle="page.stepTwo"
                  :stepText="page.stepTwoText"
                  :stepTextTwo="page.stepTwoTextTwo"
                  stepImage="https://alexborecky.com/images/banner-image.png">

                  <!-- ADDITIONAL STEP TWO CONTENT -->
                  <div slot="stepContent">

                    <p>
                      Podívejme se znovu na náš kód, který budeme vkládat do administrace Shoptetu.
                    </p>

                    <iframe class="codepen"
                      height="320" 
                      style="width: 100%; border: none"  
                      src="https://codepen.io/alexborecky/embed/xxVOyQb?height=231&theme-id=dark&default-tab=html">
                    </iframe>

                    <p> 
                      V první v řadě změníme obsah za textem <span class="orange-text"> src </span> v <span class="yellow-text"><span class="yellow-text">&lt;</span>img&gt;</span> atributu a mezi uvozovkami, který reprezentuje obrázek, jenž je v pozadí banneru.
                    </p>

                    <pre slot="additionalContent"><code class="green-text"> <br>   https://shoptet.tomashlad.eu/user/documents/extras/opal/img/banner1.png</code>
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
                  stepImage="https://alexborecky.com/images/banner-text.png">

                  <div slot="stepContent">
                    <p> Nahrazení textu je snažší, neboť se můžeme orientovat podle již zkopírovaného textu, konkrétně 
                      <span class="yellow-text"> Nahradíme nadpisem </span> a 
                      <span class="yellow-text"> Nahradíme popiskem </span> v attrbitutech 
                      <span class="yellow-text"><span class="yellow-text">&lt;</span>h3&gt;</span> a 
                      <span class="yellow-text"><span class="yellow-text">&lt;</span>p&gt;</span>.</p> 
                    
                    <pre slot="additionalContent"><code class="yellow-text"> <br>   <span class="yellow-text">&lt;</span><span>h3&gt;</span><span class="white-text">Nahradíme nadpisem</span><span>&lt;</span>/h3&gt;<br>   <span class="yellow-text">&lt;</span><span>p&gt;</span><span class="white-text">Nahradíme popiskem</span><span>&lt;</span>/p&gt;</code>
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
                  stepImage="https://alexborecky.com/images/banner-text.png">

                  <div slot="stepContent">
                    <p> Podíváme se na zoubek obsahu mezi uvozovkami 
                      <span class="orange-text"> href </span> v atribtutu 
                      <span class="yellow-text"><span class="yellow-text">&lt;</span>a></span>, 
                      který reprezentuje link / adresu, kam bude tlačítko směřovat. V tuto chvíli máme na tomto místě pouze vyplněný hashtag #.
                    </p>

                    <pre slot="additionalContent">
                      <code class="green-text"> <br>  href="#"</code>
                    </pre> 

                    <p>
                      Tento hashtag nahradíme adresou, na kterou chceme aby tlačítko banneru směřovalo. Pokud směřuje na slevu, či prodkut na vašem e-shopu, pak stačí nahradit # adresou konkrétní stranky produktu, či jiné.
                    </p>
                    
                    <p>
                      Druhá část je text, který definuje text tlačítka v banneru. V našem případě je to nyní 
                      <span class="yellow-text">Kliknutí na odkaz</span>
                    </p>

                    <pre>
                      <code class="white-text"><br>   <span class="yellow-text">&lt;</span><span class="yellow-text">a</span> <span class="orange-text">href</span>=<span class="green-text">"#"</span> <span class="orange-text">class</span>=<span class="green-text">"button"</span><span class="yellow-text">></span>Kliknutí na odkaz<span class="yellow-text"><span>&lt;</span>/a></span></code>
                    </pre>

                    <p>
                      Nahradíme-li tento text jakýmkoliv, který bude příznačný pro konkrétní tlačítko, změna se nám projeví.
                    </p>
                  </div>

              </step>
            </div>
          </additionalContent>
            <footerNavigation 
            :previousArticle="page.chapterOne"
            :nextArticle="page.chapterThree"
            nextUrl="/banners"
            previousUrl="/images"
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
  name: 'banners',
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
