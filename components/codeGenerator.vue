<template>
    <div class="code-generator">
        <div class="inputs flex column">

            <h4>{{codeTitle}}</h4>
            <p>{{codeDescription}}</p>

            <div class="input-field flex column">
                <label for="">Adresa obrázku</label>
                <input type="text" placeholder="Adresa obrázku" v-model="url">
            </div>

            <div class="input-field flex column">
                <label for="">Nadpis banneru</label>
                <input type="text" placeholder="Nadpis banneru" v-model="title">
            </div>

            <div class="input-field flex column">
                <label for="">Popisek banneru</label>
                <input type="text" placeholder="Popisek banneru" v-model="description">
            </div>
            
            <div class="input-field flex column">
                <label for="">URL Tlačítka</label>
                <input type="text" placeholder="Adresa Tlačítka" v-model="buttonUrl">
            </div>

            <div class="input-field flex column">
                <label for="">Text Tlačítka</label>
                <input type="text" placeholder="Text tlačítka" v-model="buttonText">
            </div>
        </div>
        <div class="output">
            <label for="">{{bannerType}}</label>
            <pre>
                <code class="lowered-code">
                    <div class="wrapper lowered-code">
                        &lt;div  class="{{bannerClass}}"> <br>
                        <div class="wrapper lowered-code">
                        &lt;img src="<span class="white-text">{{url}}</span>"> <br>
                            <div class="wrapper lowered-code">
                                &lt;div class="banner-caption"> <br>
                                <div class="wrapper lowered-code">
                                    &lt;{{heading}}><span class="white-text">{{title}}</span>&lt;/{{heading}}> <br>
                                    &lt;p><span class="white-text">{{description}}</span>&lt;/p> <br>
                                </div>
                                &lt;a href="<span class="white-text">{{buttonUrl}}</span>" class="button"><span class="white-text">{{buttonText}}</span>&lt;/a> <br>
                            </div>
                        &lt;/div> <br>
                        </div>
                        &lt;/div>
                    </div>
                </code>
                <!-- <button type="button"
                    v-clipboard:copy="message"> 
                    Copy!
                </button> -->
            </pre>
        </div>
    </div>
</template>


<script>
export default {
    name: 'codeGenerator',
    data () {
        return {
            name: 'myName',
            url: 'https://shoptet.tomashlad.eu/user/documents/extras/opal/img/banner1.png',
            title: 'Nahradíme nadpisem',
            description: 'Nahradíme popiskem',
            buttonUrl: '#',
            buttonText: 'Kliknutí na odkaz',
            message: 'Hello there'
        }
    },
    props: [
        'codeTitle',
        'codeDescription',
        'bannerClass',
        'heading',
        'bannerType'
    ],
}
</script>


<style lang="scss" scoped>

.code-generator {
    margin: 32px 0;
}

p {
    margin: 32px 0;
}
    
input {
    width: 100%;
    height: 40px;
    border: solid 2px rgba($color: black, $alpha: .2);
    border-radius: 5px;
    &[type=text] {
        padding-left: 16px;
        color: $blue-color;
        font-weight: 600;
    }
}

.input-field {
    margin: 8px 0;
}

.output {
    margin: 24px 0;
}

pre {
    white-space: nowrap;
    overflow: auto;
    margin: 0;
    code {
        margin: 24px;
        .wrapper {
            margin-left: 24px;
        }
    }
    button {
        margin: 24px;
        float: right;
    }
}

</style>