<template>
    <v-footer color="grey lighten-4 pt-10 pb-9">
        <div class="grid">
            <!-- Policy Link -->
            <thirdFooterPoliLink></thirdFooterPoliLink>
            <!-- Policy Images -->
            <thirdFooterPolimg></thirdFooterPolimg>
            <!-- Policy Companies -->
            <thirdFooterCompanies></thirdFooterCompanies>
        </div>
    </v-footer>
</template>

<script>
import thirdFooterPoliLink from './thirdFooterPoliLink.vue';
import thirdFooterPolimg from './thirdFooterPolimg.vue';
import thirdFooterCompanies from './thirdFooterCompanies.vue';

export default {
    name: 'thirdFooterIndex',
    components: {
        thirdFooterPoliLink,
        thirdFooterPolimg,
        thirdFooterCompanies,
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

.grid-column-2-4 {
    width: 20%;
}
</style>