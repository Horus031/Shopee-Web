<template>
    <div>
        <!-- Product Advertisements -->
        <bodyProductAds></bodyProductAds>

        <!-- Product Categories -->
        <bodyProductCategory></bodyProductCategory>
    </div>
</template>

<script>
import bodyProductAds from './bodyProductAds.vue';
import bodyProductCategory from './bodyProductCategory.vue';

export default {
    name: 'productBody',
    components: {
        bodyProductAds,
        bodyProductCategory,
    },
    data() {
        return {            
            
        }
    },
};



</script>

<style scoped>
</style>