<template>
    <div class="snackbar flex full-width">
        <div class="snackbar-content flex">
            <div class="flex snack-col">
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="3" stroke-linecap="round" stroke-linejoin="round" class="feather feather-alert-circle"><circle cx="12" cy="12" r="10"></circle><line x1="12" y1="8" x2="12" y2="12"></line><line x1="12" y1="16" x2="12.01" y2="16"></line></svg>
            </div>
            <div class="flex column text">
                <h5>{{snackBarText}}</h5>
                <nuxt-link :to="snackUrl">{{snackBarLink}}</nuxt-link> 
            </div>
        </div>
    </div>
</template>


<script>
export default {
    name: 'snackbar',
    props: ['snackBarText', 'snackBarLink', 'snackUrl']
}
</script>


<style lang="scss" scoped>

.snackbar {
    margin-top: 24px;
    border-left: solid 3px $blue-color;
    background-color: rgba($color: $blue-color, $alpha: .2);
    .snackbar-content {
        padding: 24px 0;
        .text {
            margin-right: 16px;
        }
        h5 {
            color: $blue-color;
            max-width: 650px;
        }
        svg {
            stroke: $blue-color;
        }
        a {
            color: $blue-color;
            text-decoration: underline;
            margin-top: 24px;
        }
        @media only screen and (max-width: 450px) {
            // flex-flow: column;
            .snack-col {
                margin: 4px 8px;
            }
        }
    }
}

.warning {
    border-left: solid 3px $warning-orange;
    background-color: rgba($color: $warning-orange, $alpha: .2);
    .snackbar-content {
        h5 {
            color: $warning-orange;
        }
        svg {
            stroke: $warning-orange;
        }
    }
}

.alert {
    border-left: solid 3px $alert-red;
    background-color: rgba($color: $alert-red, $alpha: .2);
    .snackbar-content {
        h5 {
            color: $alert-red;
        }
        svg {
            stroke: $alert-red;
        }
    }
}

.success {
    border-left: solid 3px $success-green;
    background-color: rgba($color: $success-green, $alpha: .2);
    .snackbar-content {
        h5 {
            color: $success-green;
        }
        svg {
            stroke: $success-green;
        }
        a {
            color: $success-green;
        }
    }
}

.no-link {
    a {
        display: none;
    }
}
    
</style>