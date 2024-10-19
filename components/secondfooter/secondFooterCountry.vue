<template>
    <!-- Country Footer -->
    <div>
        <v-sheet class="d-flex justify-space-between py-10" color="transparent">
            <span class="mr-6 subtitle-2 grey--text text--darken-2 font-weight-light">© 2024 Shopee. Tất cả các quyền được bảo lưu.</span>
            <div class="d-flex">
                <div class="subtitle-2 grey--text text--darken-2 font-weight-light">
                    <span>Quốc gia & Khu vực:</span>
                    <span>
                        <span v-for="(country, index) in countryList" :key="index">
                            <a href="" class="text-decoration-none grey--text text--darken-2 font-weight-light">{{ country.name }}</a>
                            <template v-if="index < countryList.length - 1"> | </template>
                        </span>
                    </span>
                </div>
            </div>
        </v-sheet>
    </div>
</template>

<script>
export default {
    name: 'secondFooterCountry',
    data() {
        return {
            countryList: [
                { name: 'Singapore' },
                { name: 'Indonesia' },
                { name: 'Thái Lan' },
                { name: 'Malaysia' },
                { name: 'Việt Nam' },
                { name: 'Philippines' },
                { name: 'Brazil' },
                { name: 'México' },
                { name: 'Colombia' },
                { name: 'Chile' },
                { name: 'Đài Loan' },
            ],
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