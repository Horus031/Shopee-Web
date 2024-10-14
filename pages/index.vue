<template>
    <v-app light>
        <!-- Header Navbar Wrapper-->
        <headerNavbar></headerNavbar>

        <!-- Products Body -->
        <productBody></productBody>

        <!-- First Footer -->
        <firstFooter></firstFooter>

        <!-- Second Footer -->
        <secondFooter></secondFooter>

        <!-- Third Footer -->
        <thirdFooter></thirdFooter>
    </v-app>
</template>

<script>
import headerNavbar from '../components/headerNavbar.vue';
import productBody from '../components/productBody.vue';
import firstFooter from '../components/firstFooter.vue';
import secondFooter from '../components/secondFooter.vue';
import thirdFooter from '../components/thirdFooter.vue';

  export default {
    components: {
        headerNavbar,
        productBody,
        firstFooter,
        secondFooter,
        thirdFooter,
    },
    
}
</script>

<style>

</style>