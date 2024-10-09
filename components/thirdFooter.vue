<template>
    <v-footer color="grey lighten-4 pt-10 pb-9">
        <div class="grid">
            <!-- Policy Link -->
            <div class="mb-10 d-flex justify-center caption font-weight-light">
                <div class="px-6">
                    <a href="" class="grey--text text--darken-2 text-decoration-none">CHÍNH SÁCH BẢO MẬT</a>
                </div>
                <div class="px-6">
                    <a href="" class="grey--text text--darken-2 text-decoration-none">QUY CHẾ HOẠT ĐỘNG</a>
                </div>
                <div class="px-6">
                    <a href="" class="grey--text text--darken-2 text-decoration-none">CHÍNH SÁCH VẬN CHUYỂN</a>
                </div>
                <div class="px-6">
                    <a href="" class="grey--text text--darken-2 text-decoration-none">CHÍNH SÁCH TRẢ HÀNG VÀ HOÀN TIỀN</a>
                </div>
            </div>

            <!-- Policy Image -->
            <div class="d-flex justify-center align-center mt-0">
                <a href="" class="px-5">
                    <v-img
                        :src="require('@/assets/img/registered_policy.png')"
                        max-height="45px"
                        contain
                        position="center center"    
                    >

                    </v-img>
                </a>
                <a href="" class="px-5">
                    <v-img
                        :src="require('@/assets/img/registered_policy.png')"
                        max-height="45px"
                        contain
                        position="center center"    
                    >

                    </v-img>
                </a>
                <a href="" class="px-5">
                    <v-img
                        :src="require('@/assets/img/handprint_policy.png')"
                        max-height="45px"
                        contain
                        position="center center"    
                    >

                    </v-img>
                </a>
            </div>

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
    </v-footer>
</template>

<script>
export default {
    name: 'thirdFooter',

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

<style scoped>

.grid {
    width: 1200px;
    max-width: 100%;
    margin: 0 auto;
}

.grid-column-2-4 {
    width: 20%;
}

.v-list-item__title, .v-list-item__subtitle {
    overflow: visible !important;
}

.v-list-item__content {
    flex: none;
    align-self: normal;
    padding: 6px 0;
}

.item-first {
    padding-top: 16px;
}

.header__navbar-item--separator::after {
    content: "";
    display: block;
    position: absolute;
    width: 1px;
    height: 13px;
    background-color: #fb9086;
    right: 0;
    top: 50%;
    transform: translateY(-50%);
}

.header__navbar-item {
    position: relative;
}

::v-deep .v-input__control {
    height: 40px !important;
}




</style>