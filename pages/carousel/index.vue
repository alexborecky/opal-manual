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
        <intro/>
        <nuxt-content :document="page"></nuxt-content>
        <!-- NASTAVENI CAROUSELU -->
        <videoTutorial id="carousel"
          :sectionTitle="page.chapterThree"
          :sectionDescription="name1">
          <div slot="codepen">
            <iframe 
              height="260" 
              style="width: 100%; border: none"  
              src="https://codepen.io/alexborecky/embed/xxVOyQb?height=231&theme-id=dark&default-tab=html">
            </iframe>
          </div> 
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
