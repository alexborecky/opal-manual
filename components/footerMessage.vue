<template>
    <div class="full-width footer-message">
        <snackBar class="success"
            :snackBarText="snackBarMessage"
        />
        <h5>{{footerMessage}}</h5>
    </div>
</template>


<script>
export default {
    name: 'footerMessage',
    data () {
        return {
            snackBarText: 'Hello'
        }
    },
    props: [
        'snackBarMessage',
        'footerMessage'
    ]
}
</script>


<style lang="scss" scoped>
    
</style>