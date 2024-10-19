<template>
    <v-footer color="grey lighten-5">
        <div class="grid">

            <!-- Information Footer -->
            <secondFooterInfor></secondFooterInfor>

            <v-divider></v-divider>

            <!-- Country Footer-->
            <secondFooterCountry></secondFooterCountry>
        </div>
    </v-footer>
</template>

<script>
import secondFooterInfor from './secondFooterInfor.vue';
import secondFooterCountry from './secondFooterCountry.vue';

export default {
    name: 'secondFooterIndex',
    components: {
        secondFooterInfor,
        secondFooterCountry,
    },
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