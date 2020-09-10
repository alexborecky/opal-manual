<template>
    <div class="full-width flex center link-footer">
        <div class="container flex">
            <div class="flex column category">
                <h5>Odkazy</h5>
                <a href="https://shoptet.cz" target="_blank">Zpět do Shoptet.cz</a>
                <a href="https://shoptetak.cz" target="_blank">Shoptetak.cz</a>
            </div>
            <div class="flex column category">
                <h5>Kontakt</h5>
                <a href="mailto:info@shoptetak.cz" target="_blank">Email</a>
                <a href="https://www.facebook.com/Shoptetakcz-380301622541841/" target="_blank">Facebook</a>
            </div>
            <div class="flex column category">
                <h5>Soukromí</h5>
                <nuxt-link to="/gdpr" target="_blank">GDPR</nuxt-link> 
            </div>
        </div>
    </div>
</template>



<script>
export default {
    name: 'linkFooter'
}
</script>


<style lang="scss" scoped>

.link-footer {
   .container {
        justify-content: space-between;
        align-items: flex-start;
        border-top: solid rgba($color: lightgray, $alpha: .6) 1px;
        @media only screen and (max-width: 450px) {
            flex-flow: column;
            align-items: center;
        }
        .category {
            text-align: center;
            h5 {
                text-transform: uppercase;
                font-weight: 800;
                margin: 32px 0 8px 0;
                color: $blue-color;
            }
            a {
                opacity: .4;
                margin: 4px 0;
                &:hover {
                    opacity: .8;
                    color: black;
                }
            }
        }
    } 
}


    
</style>