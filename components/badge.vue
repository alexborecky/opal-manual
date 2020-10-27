<template>
    <div class="badge">
       Již brzy
    </div>
</template>

<script>
    export default {
        name: 'badge'
    }
</script>

<style lang="scss" scoped>

.badge {
    background-color: rgba($color: $shop-orange, $alpha: .08);
    color: $shop-orange;
    padding: 2px 8px;
    font-size: 12px;
    font-weight: 600;
    border-radius: 4px;
    margin-left: 16px;
    display: none;
}

.see-badge {
  .badge {
    display: block !important;
  }
}

</style>