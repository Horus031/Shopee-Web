<template>
    <header class="header">
            <div class="grid">
                <!-- Navbar -->
                <headerNavbar></headerNavbar>
                <!-- Header with search -->
                 <headerWithSearch></headerWithSearch>
            </div>
    </header>
</template>

<script>
import headerNavbar from './headerNavbar.vue';
import headerWithSearch from './headerWithSearch.vue';

export default {
    name: 'headerIndex',
    components: {
        headerNavbar,
        headerWithSearch,
    },
    data() {
        return {
            hover: false,
        };
    },
};
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

.header {
    background-image: linear-gradient(-180deg, #f53d2d, #f63); 
    position: fixed;
    height: 120px; 
    top:0; 
    left:0; 
    bottom:0; 
    right:0; 
    z-index:8;
}

</style>