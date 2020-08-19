<template>
    <div class="full-width flex column image-tutorial">
        <div class="text-content">
            <h3>{{sectionTitle}} <div class="underline"></div> </h3>
            <p>{{sectionDescription}}</p>
        </div>
    </div>
</template>



<script>
export default {
    name: 'textTutorial',
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
        .underline {
            height: 6px;
            width: 120px;
            opacity: .8;
            background-color: black;
            border-radius: 100px;
        }
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
        }
    }
}
    
</style>