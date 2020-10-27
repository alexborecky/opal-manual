<template>
    <nuxt-link :to="tempLink" class="product-card flex column">
        <div class="product-image">
            <svg width="240" height="120" viewBox="0 0 240 120" fill="none" xmlns="http://www.w3.org/2000/svg">
            <g clip-path="url(#clip0)">
            <rect x="0.5" y="0.5" width="239" height="119" rx="7.5" fill="#DBE1EC" fill-opacity="0.16" stroke="#DBE1EC" stroke-width="2"/>
            <path d="M98.75 80.25H259.25M152.25 187.25V80.25M116.583 26.75H241.417C251.266 26.75 259.25 34.7343 259.25 44.5833V169.417C259.25 179.266 251.266 187.25 241.417 187.25H116.583C106.734 187.25 98.75 179.266 98.75 169.417V44.5833C98.75 34.7343 106.734 26.75 116.583 26.75Z" stroke="#1E1E1C" stroke-opacity="0.6" stroke-width="4" stroke-linecap="round" stroke-linejoin="round"/>
            </g>
            <defs>
            <clipPath id="clip0">
            <rect width="240" height="120" fill="white"/>
            </clipPath>
            </defs>
            </svg>
        </div>
        <div class="product-content">
            <div class="title flex">
                <h5>{{tempTitle}}</h5>
                <badge />
            </div>
            <p class="small">{{tempDes}}</p>
        </div>
    </nuxt-link>
</template>

<script>
    export default {
        name: 'templateCard',
        props: [
            'tempTitle',
            'tempDes',
            'tempLink',
        ]
    }
</script>

<style lang="scss" scoped>

</style>