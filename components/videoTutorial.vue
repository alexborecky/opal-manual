<template>
    <div class="full-width flex column video-tutorial">
        <div class="text-content">
            <h3>{{sectionTitle}} <div class="underline"></div> </h3>
            <p>{{sectionDescription}}</p>
            <div class="video flex center">
                <div class="video-slot">
                    <slot class="video-slot" name="youtube"></slot>
                </div>
            </div>
            <p>{{sectionDescriptionTwo}}</p>
            <slot name="codepen"></slot>
            <p>{{sectionDescriptionThree}}</p>
        </div>
        <slot name="additionalContent"></slot>
    </div>
</template>



<script>
export default {
    name: 'videoTutorial',
    props: [
        'url', 
        'sectionTitle', 
        'sectionDescription', 
        'sectionDescriptionTwo', 
        'sectionDescriptionThree', 
        'stepOne', 
        'stepOneText', 
        'stepOneTextTwo', 
        'stepOneImage',
        'stepTwo',
        'stepTwoText',
        'stepTwoImage',
        'stepTwoTextTwo',
        'stepThree',
        'stepThreeText',
        'stepThreeImage',
        'stepThreeTextTwo',
        'stepFour',
        'stepFourText',
        'stepFourImage',
        'stepFourTextTwo',
        ]
}
</script>


<style lang="scss" scoped>

.text-content {
    h3 {
        margin: 0 0 40px 0;
    }
}

.video-tutorial {
    min-height: 50vh;
    margin: 80px 0 0 0;
    .video {
        margin: 40px 0;
        height: 480px;
        width: 100%;
        .video-slot {
            width: 100%;
            height: 100%;
        }
    }
        p {
        margin: 32px 0 0 0;
    }
    .underline {
        height: 6px;
        width: 120px;
        opacity: .8;
        background-color: black;
        border-radius: 100px;
    }
    h4 {
        .underline {
            width: 80px;
        }
    }
}
    
</style>