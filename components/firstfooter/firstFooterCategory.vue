<template>
    <div>
        <v-sheet class="mt-15 mb-8 pb-15">
            <div class="subtitle-2 grey--text darken-2">Danh Mục</div>
            <div class="row" style="margin: -10px -5px 0 -5px;">
                <!-- Categories Column 1 -->
                <footerCategoriesCol1 class="grid-column-2-4"></footerCategoriesCol1>
                <!-- Categories Column 2 -->
                <footerCategoriesCol2 class="grid-column-2-4"></footerCategoriesCol2>
                <!-- Categories Column 3 -->
                <footerCategoriesCol3 class="grid-column-2-4"></footerCategoriesCol3>
                <!-- Categories Column 4 -->
                <footerCategoriesCol4 class="grid-column-2-4"></footerCategoriesCol4>
                <!-- Categories Column 5 -->
                <footerCategoriesCol5 class="grid-column-2-4"></footerCategoriesCol5>
            </div>
        </v-sheet>
    </div>
</template>

<script>
import footerCategoriesCol1 from './footerCategories/categoriesCol1.vue';
import footerCategoriesCol2 from './footerCategories/categoriesCol2.vue';
import footerCategoriesCol3 from './footerCategories/categoriesCol3.vue';
import footerCategoriesCol4 from './footerCategories/categoriesCol4.vue';
import footerCategoriesCol5 from './footerCategories/categoriesCol5.vue';

export default {
    name: 'firstFooterCategory',
    components: {
        footerCategoriesCol1,
        footerCategoriesCol2,
        footerCategoriesCol3,
        footerCategoriesCol4,
        footerCategoriesCol5,
    }
    
}
</script>

<style scoped>
* {
    font-family: Arial, Helvetica, sans-serif;
}

.grid {
    width: 1200px;
    max-width: 100%;
    margin: 0 auto;
}

.grid-column-2-4 {
    width: 20%;
}
</style>