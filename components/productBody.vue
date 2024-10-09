<template>
    <v-sheet color="white" style="margin-top: 120px">
        <div class="grid">
            <h1 class="text-center">Product Body</h1>
            <h1 class="text-center">Chua lam gi het</h1>
        </div>
    </v-sheet>
</template>

<script>
export default {
    name: 'productBody',
}
</script>

<style scoped>

.grid {
    width: 1200px;
    max-width: 100%;
    margin: 0 auto;
}

.grid-column-2-4 {
    width: 20%;
}

.v-list-item__title, .v-list-item__subtitle {
    overflow: visible !important;
}

.v-list-item__content {
    flex: none;
    align-self: normal;
    padding: 6px 0;
}

.item-first {
    padding-top: 16px;
}

.header__navbar-item--separator::after {
    content: "";
    display: block;
    position: absolute;
    width: 1px;
    height: 13px;
    background-color: #fb9086;
    right: 0;
    top: 50%;
    transform: translateY(-50%);
}

.header__navbar-item {
    position: relative;
}

::v-deep .v-input__control {
    height: 40px !important;
}


</style>