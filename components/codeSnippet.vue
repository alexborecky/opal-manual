<template>
    <pre class="code-snippet">
        <code>
            <div class="wrapper">
                <div class="first-layer">
                    &lt;<span class="red">div</span>  <span class=yellow>class</span>="<span class="green">{{bannerClass}}</span>"> 
                </div>
                    <div class="second-layer">
                        &lt;<span class="red">img</span> <span class="yellow">src</span>="<span class="green">{{imageUrl}}</span>"> 
                    </div>
                        <div class="second-layer">
                            &lt;<span class="red">div</span> <span class="yellow">class</span>="<span class="green">{{bannerClassTwo}}</span>"> 
                        </div>
                            <div class="third-layer">
                                &lt;<span class="red">{{heading}}</span>><span class="white">{{title}}</span>&lt;/<span class="red">{{heading}}</span>>
                            </div>
                            <div class="third-layer">
                                &lt;<span class="red">p</span>><span class="white">{{description}}</span>&lt;/<span class="red">p</span>>
                            </div>
                            <div class="third-layer">
                                &lt;<span class="red">a</span> <span class="yellow">href</span>="<span class="green">{{buttonUrl}}</span>" <span class="yellow">class</span>="<span class="green">button</span>"><span class="white">{{buttonText}}</span>&lt;/<span class="red">a</span>> 
                            </div>
                    <div class="second-layer">
                        &lt;/<span class="red">div</span>>
                    </div>
                    <slot name="extraCode"></slot>
                <div class="first-layer">
                    &lt;/<span class="red">div</span>>
                </div>
                <slot name="additionalCode"></slot>
            </div>   
        </code>
    </pre>
</template>

<script>
export default {
    name: 'codeSnippet',
    props: [
        'heading',
        'title',
        'description',
        'buttonText',
        'buttonUrl',
        'bannerClass',
        'bannerClassTwo',
        'imageUrl'
    ]
}
</script>

<style lang="scss" scoped>

.code-snippet {
    margin-top: 32px;
}
    
</style>