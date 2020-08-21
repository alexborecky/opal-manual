<template>
    <div class="intro flex column">
        <div class="introduction-content">
            <h1>{{templateTitle}}</h1>
            <p>{{introDescription}}</p>
        </div>
        <div class="image flex center bottom-end"></div>
        <div class="overview">
            <article>
                <h3>{{introSubtitle}}</h3>
                <p>{{introSubtextOne}}</p>
                <p>{{introSubtextTwo}}</p>
            </article>
            <snackBar class="warning no-link"
                :snackBarText="introSnackBar"
                :snackUrl="introSnackUrl"
                :snacBarLink="introSnackLink"
            />
        </div>
    </div>
</template>



<script>
export default {
    name: 'intro',
    data () {
        return {
            text: 'Hello'
        }
    },
    props: [
        'introSnackBar', 
        'introSnackUrl', 
        'introSnackLink',
        'templateTitle',
        'introDescription',
        'introSubtitle',
        'introSubtextOne',
        'introSubtextTwo'
        ]
}
</script>

<style lang="scss" scoped>

.intro {
    width: 100%;
    margin-top: 80px;
    h1 {
        margin-bottom: 24px;
    }
}

.introduction-content {
    height: 100%;
    h4 {
        margin-bottom: -24px;
    }
    p {
        max-width: 650px;
        font-weight: 600;
        margin-top: 8px;
    }
}

.overview {
    article {
        p {
            margin: 32px 0;
        }
    }
}

.image {
    margin: 40px 0;
    background-image: url(https://alexborecky.com/images/opal.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    height: 500px;
    width: 100%;
}
    
</style>