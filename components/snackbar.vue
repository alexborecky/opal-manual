<template>
    <div class="snackbar full-width">
        <div class="snackbar-content flex">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="3" stroke-linecap="round" stroke-linejoin="round" class="feather feather-alert-circle"><circle cx="12" cy="12" r="10"></circle><line x1="12" y1="8" x2="12" y2="12"></line><line x1="12" y1="16" x2="12.01" y2="16"></line></svg>
            <h5>{{snackBarText}}</h5>
        </div>
    </div>
</template>


<script>
export default {
    name: 'snackbar',
    props: ['snackBarText']
}
</script>


<style lang="scss" scoped>

.snackbar {
    margin-top: 24px;
    border-left: solid 3px $blue-color;
    background-color: rgba($color: $blue-color, $alpha: .2);
    .snackbar-content {
        margin-left: 24px;
        padding: 24px 0;
        img {
            height: 24px;
            width: 24px;
            margin: 0;
        }
        h5 {
            margin-left: 16px;
            color: $blue-color;
        }
        svg {
            stroke: $blue-color;
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
    
</style>