<template>
    <v-footer color="white" style="border-top: 4px solid #ee4d2d !important;">
        <div class="grid">
            
            <firstFooterAbstract></firstFooterAbstract>

            <v-divider></v-divider>

            <firstFooterCategory></firstFooterCategory>

        </div>
    </v-footer>
</template>

<script>
import firstFooterAbstract from './firstFooterAbstract.vue';
import firstFooterCategory from './firstFooterCategory.vue';

export default {
    name: 'firstFooterIndex',
    components: {
        firstFooterAbstract,
        firstFooterCategory,
    },
    data() {
        return {
        }
    }
}
</script>

<style scoped>

.grid {
    width: 1200px;
    max-width: 100%;
    margin: 0 auto;
}

</style>