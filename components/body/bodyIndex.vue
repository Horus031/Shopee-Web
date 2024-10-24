<template>
    <v-sheet>
        <!-- Product Advertisements -->
        <bodyProductAds></bodyProductAds>

        <v-sheet color="grey lighten-4">
            <!-- Free Advertisement -->
            <bodyFreeAds></bodyFreeAds>

            <!-- Product Categories -->
            <bodyProductCategory></bodyProductCategory>
        </v-sheet>
    </v-sheet>
</template>

<script>
import bodyProductAds from './bodyProductAds.vue';
import bodyProductCategory from './bodyProductCategory.vue';
import bodyFreeAds from './bodyFreeAds.vue';

export default {
    name: 'productBody',
    components: {
        bodyProductAds,
        bodyProductCategory,
        bodyFreeAds,
    },
    data() {
        return {            
            
        }
    },
};



</script>

<style>
</style>