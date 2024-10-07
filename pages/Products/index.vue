<template>
    <div>
        products
    </div>
</template>

<script>
import { mapFields } from "vuex-map-fields";

export default {
    data() {
        return {
            conheo: ''
        }
    },
    mounted() {

        if (this.token) {
            console.log('co')
            $axios.defaults.headers.common['Authorization'] = `Bearer ${this.token}`;
        }
        else console.log('ngu')
    },
    computed: {
        ...mapFields("storeToken", ["tokenNe"]),

    },
};
</script>

<style></style>