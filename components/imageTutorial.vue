<template>
    <div class="full-width flex column image-tutorial">
        <div class="text-content">
            <h3>{{sectionTitle}} <div class="underline"></div> </h3>
            <p>{{sectionDescription}}</p>
        </div>
        <div class="image flex center">
            <div :style="{backgroundImage: 'url(' + tutorialImage + ')'}" class="image-slot">
            </div>
        </div>
        <slot name="additionalContent"></slot>
    </div>
</template>



<script>
export default {
    name: 'videoTutorial',
    props: ['url', 'sectionTitle', 'sectionDescription', 'tutorialImage']
}
</script>


<style lang="scss" scoped>

.text-content {
    p {
        margin: 20px 0;
    }
    h3 {
        margin: 0 0 40px 0;
    }
}

.image-tutorial {
    // min-height: 50vh;
    margin-top: 80px;
    .image {
        .image-slot {
            height: 480px;
            width: 100%;
            margin: 40px 0;
            background-position: center;
            background-size: cover;
            @media only screen and (max-width: 450px) {
                height: 240px;
            }
        }
    }
}
    
</style>