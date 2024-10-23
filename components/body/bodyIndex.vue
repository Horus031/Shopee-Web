<template>
    <div>
        <!-- Product Advertisements -->
        <bodyProductAds></bodyProductAds>

        <!-- Free Advertisement -->
         <bodyFreeAds></bodyFreeAds>

        <!-- Product Categories -->
        <bodyProductCategory></bodyProductCategory>
    </div>
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

<style scoped>
</style>