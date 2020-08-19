<template>
    <div class="footer-navigation full-width flex">
        <nuxt-link :to="previousUrl">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-arrow-left"><line x1="19" y1="12" x2="5" y2="12"></line><polyline points="12 19 5 12 12 5"></polyline></svg>
            {{previousArticle}}
        </nuxt-link>

        <nuxt-link :to="nextUrl">
            {{nextArticle}}
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-arrow-right"><line x1="5" y1="12" x2="19" y2="12"></line><polyline points="12 5 19 12 12 19"></polyline></svg>
        </nuxt-link>

    </div>
</template>


<script>
export default {
    name: 'footerNavigation',
    props: [
        'previousUrl',
        'nextUrl',
        'previousArticle',
        'nextArticle'
    ]
}
</script>


<style lang="scss" scoped>

.footer-navigation {
    margin: 40px 0 0 0;
    height: 80px;
    justify-content: space-between;
    align-items: center;
    a {
        color: $blue-color;
        display: flex;
        justify-content: center;
        align-items: center;
        svg {
            height: 16px;
        }
        &:hover {
            svg {
                stroke-width: 3;
            }
        }
    }
}
    
</style>