<template>
    <div class="content-list flex center-left">
        <div class="content">
            <h4>Obsah</h4>
            <ul>
                <li><nuxt-link to="/">{{introContent}}</nuxt-link></li>
                <li><nuxt-link to="/images">{{contentOne}}</nuxt-link></li>
                <li><nuxt-link to="/banners">{{contentTwo}}</nuxt-link></li>
                <li><nuxt-link to="/carousel">{{contentThree}}</nuxt-link></li>
                <li><nuxt-link to="/social-media">{{contentFour}}</nuxt-link></li>
                <li><nuxt-link to="/logos">Ikony platebních metod</nuxt-link></li>
                <li><nuxt-link to="/amount">{{contentSeven}}</nuxt-link></li>
                <br> <br> 
                <li><nuxt-link to="/generator">{{contentSix}}<span> (beta)</span></nuxt-link></li>
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
        @media only screen and (max-width: 800px) {
            display: none;
        }
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
            padding: 8px 0;
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

