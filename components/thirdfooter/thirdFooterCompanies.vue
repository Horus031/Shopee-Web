<template>
    <div>
        <!-- Company -->
        <div class="caption d-block text-center mt-2 mb-6 grey--text text--darken-2 font-weight-light">Công ty TNHH Shopee</div>

        <div class="mt-2">
            <span class="caption grey--text text--darken-2 font-weight-light d-block text-center">
                <span v-for="(address, index) in addresses" :key="index">
                    Địa chỉ:
                    <span>{{ address.name }}</span>
                </span>
                <span v-for="(hotline, index) in hotlineAndEmail" :key="index">
                    Tổng đài hỗ trợ:
                    <span>{{ hotline.name }}</span>
                </span>
            </span>
        </div>

        <div class="mt-2 caption d-block text-center grey--text text--darken-2 font-weight-light">
            Chịu Trách Nhiệm Quản Lý Nội Dung: Nguyễn Bùi Anh Tuấn
        </div>
        <div class="mt-2 caption d-block text-center grey--text text--darken-2 font-weight-light">
            Mã số doanh nghiệp: 0106773786 do Sở Kế hoạch & Đầu tư TP Hà Nội cấp lần đầu ngày 10/02/2015
        </div>
        <div class="mt-2 caption d-block text-center grey--text text--darken-2 font-weight-light">
            © 2015 - Bản quyền thuộc về Công ty TNHH Shopee
        </div>
    </div>
</template>

<script>
export default {
    name: 'thirdFooterCompanies',
    data() {
        return {
            addresses: [
                { name: 'Tầng 4-5-6, Tòa nhà Capital Place, số 29 đường Liễu Giai, Phường Ngọc Khánh, Quận Ba Đình, Thành phố Hà Nội, Việt Nam.' }
            ],
            hotlineAndEmail: [
                { name: '19001221 - Email: cskh@hotro.shopee.vn'}
            ]
        }
    }
}
</script>

<style>

</style>