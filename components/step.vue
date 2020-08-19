<template>
    <div class="step">
        <h4>{{stepTitle}}</h4>
        <p>{{stepText}}</p>
        <img :src="stepImage" alt="">
        <p>{{stepTextTwo}}</p>
        <slot name="stepContent"></slot>
    </div>
</template>

<script>
export default {
    name: 'step',
    props: [
        'stepTitle',
        'stepText',
        'stepTextTwo',
        'stepImage'
    ]
}
</script>


<style lang="scss" scoped>
    
.step {
    margin: 40px 0 0 0;
    p {
        margin: 32px 0 0 0;
    }
    img {
        margin: 32px 0 0 0;
        width: 100%;
    }
}

</style>