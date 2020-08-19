<template>
    <div class="content-list flex center-left">
        <div class="content">
            <h4>Obsah</h4>
            <ul>
                <li><nuxt-link to="/">{{introContent}}</nuxt-link></li>
                <li><nuxt-link to="/images">{{contentOne}}</nuxt-link></li>
                <li><nuxt-link to="/banners">{{contentTwo}}</nuxt-link></li>
                    <!-- <div class="subcontent">
                            <li><a href="#stepone">Krok 1: Administrace Shoptetu</a></li>
                            <li><a href="#steptwo">Krok 2: Změna obrázku</a></li>
                            <li><a href="#stepthree">Krok 3: Změna nadpisu a popisku banneru</a></li>
                            <li><a href="#stepfour">Krok 4: Změna odkazu a textu tlačítka</a></li>
                    </div> -->
                <li><a href="">{{contentThree}}</a></li>
                <li><a href="">{{contentFour}}</a></li>
                <li><a href="">{{contentFive}}</a></li> <br> <br>
                <li><a href="/generator">{{contentSix}}<span> (beta)</span></a></li>
            </ul>
        </div>
    </div>
</template>


<script>
export default {
    name: 'contentList',
    props: [
        'contentOne', 
        'contentTwo', 
        'contentThree',
        'contentFour',
        'contentFive',
        'contentSix',
        'contentSeven',
        'introContent'
        ]
}
</script>

<style lang="scss" scoped>

.content-list {
    min-height: 40vh;
    position: fixed;
    .content {
        height: 100%;
        min-width: 220px;
        position: absolute;
        right: 0;
        top: 80px;
        .subcontent {
            margin-left: 40px;
        }
    }
}

ul {
    padding-left: 0;
    margin-top: 24px;
    list-style-type: none;
    min-height: 400px;
    li {
        margin: 8px 0;
        a {
            opacity: .6;
            padding: 8px;
            &:hover {
                opacity: 1;
                color: black;
            }
        }
    }
}

.nuxt-link-exact-active {
  color: $blue-color;
  opacity: 1 !important;
  font-weight: 600;
}

span {
    font-size: 12px;
}
    
</style>

