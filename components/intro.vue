<template>
    <div class="intro flex column">
        <div class="introduction-content">
            <h1>OPAL</h1>
            <p>Předem bychom vám rádi poděkovali za důvěru vloženou v šablonu OPAL. V tomto dokumentu vás provedeme nastavením, které zaručí nejlepší vzhled vaší šablony!</p>
        </div>
        <div class="image flex center bottom-end"></div>
        <div class="overview">
            <article>
                <h3>Příprava šablony</h3>
                <p>Na této stránce naleznete veškeré informace, které vám pomohou snadněji nastavit vaší šablonu tak, aby vše fungovalo jak má a aby byl finální vzhled perfektní!</p>
                <p>Postupně vás v kapitolách z obshu provedeme nastavením tak, aby byla práce pro vás co nejsnažší.</p>
            </article>
            <snackBar class="warning"
                :snackBarText="text"
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
    }
}
</script>

<style lang="scss" scoped>

.intro {
    width: 100%;
    margin-top: 80px;
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