<template>
    <v-app light>
        <!-- Header Navbar Wrapper-->
        <headerIndex></headerIndex>

        <!-- Products Body -->
        <bodyIndex></bodyIndex>

        <!-- First Footer -->
        <firstFooterIndex></firstFooterIndex>

        <!-- Second Footer -->
        <secondFooterIndex></secondFooterIndex>

        <!-- Third Footer -->
        <thirdFooterIndex></thirdFooterIndex>

        <!-- Chat Box -->
        <chatBox></chatBox>

    </v-app>
</template>

<script>
import headerIndex from '../components/header/headerIndex.vue';
import bodyIndex from '../components/body/bodyIndex.vue';
import firstFooterIndex from '../components/firstfooter/firstFooterIndex.vue';
import secondFooterIndex from '../components/secondfooter/secondFooterIndex.vue';
import thirdFooterIndex from '../components/thirdfooter/thirdFooterIndex.vue';
import chatBox from '../components/chatBox.vue';

  export default {
    components: {
        headerIndex,
        bodyIndex,
        firstFooterIndex,
        secondFooterIndex,
        thirdFooterIndex,
        chatBox,
    },
    
}
</script>

<style>

</style>