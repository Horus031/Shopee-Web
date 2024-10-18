<template>
    <v-sheet color="white" style="margin-top: 120px">
        <div class="grid">
            <div class="d-flex pt-7 pb-3 flex-column" >
                <v-sheet class="flex-grow-1 d-flex" color="transparent" max-width="100%">
                    <!-- Product Advertisements -->
                    <v-carousel  
                        class="flex-grow-1 d-flex justify-center" 
                        cycle
                        width="auto"
                        height="235"
                        hide-delimiter-background
                        show-arrows-on-hover
                    >
                        <template v-slot:prev="{on, attrs}">
                            <v-btn
                                v-bind="attrs"
                                v-on="on"
                                width="auto"
                                height="60px"
                                class="pa-0 white--text"
                                min-width="35px"
                                tile
                            >
                                <v-icon>mdi-chevron-left</v-icon>
                            </v-btn>
                        </template>
                        <template v-slot:next="{on, attrs}">
                            <v-btn
                                v-bind="attrs"
                                v-on="on"
                                height="60px"
                                class="pa-0 white--text"
                                min-width="35px"
                                tile
                            >
                                <v-icon>mdi-chevron-right</v-icon>
                            </v-btn>
                        </template>
                        <v-carousel-item v-for="(step, index) in steps" :key="index">
                            <v-img :src="step.src" max-width="796px" height="235px" ></v-img>
                        </v-carousel-item>
                    </v-carousel>
                    
                    <v-sheet class="d-flex flex-column flex-grow-1 justify-space-between" color="transparent">
                        <div>
                            <a href="">
                                <v-img
                                src="https://cf.shopee.vn/file/sg-11134258-7rdxi-m16tffq32hr261_xhdpi"
                                max-height="115px"
                                width="388px"
                                contain
                                
                                ></v-img>
                            </a>
                        </div>
                        
                        <div>
                            <a href="">
                                <v-img
                                src="https://cf.shopee.vn/file/sg-11134258-7rdx2-m16tfhqs446155_xhdpi"
                                max-height="115px"
                                width="388px"
                                contain
                                >
                                </v-img>
                            </a>
                        </div>
                    </v-sheet>
                </v-sheet>

                <!-- Product Services -->
                <v-sheet>
                    <v-list class="pa-0">
                        <v-list-item class="pa-0 d-flex flex-nowrap justify-space-around">
                            <v-list-item-content v-for="(service, index) in services" :key="index" style="padding-top: 10px;">
                                <v-list-item-title class="d-flex justify-center align-center pa-0" style="width: auto;">
                                    <v-sheet  width="150px" min-height="108px" color="transparent" class="d-flex justify-center text-center"> <!--This to set the width-->
                                        <a href="" class="d-flex align-center flex-column text-decoration-none black--text text-wrap" style="width: 100%">
                                            <div class="mt-4 mb-2 ml-auto mr-auto d-flex justify-center"> <!-- This to set margin -->
                                                <v-img
                                                    :src="service.src"
                                                    position="center center"
                                                    width="45px"
                                                    height="45px"
                                                    contain
                                                >
                                                </v-img>
                                            </div>
                                            <div style="line-height: 1; font-size: 14px;">
                                                {{ service.name }}
                                            </div>
                                        </a>
                                        
                                    </v-sheet>
                                </v-list-item-title>
                            </v-list-item-content>
                        </v-list-item>
                    </v-list>
                </v-sheet>
            </div>
        </div>

        <!-- Product Categories -->
        <v-sheet color="grey lighten-4 pt-5" >
            <v-card class="grid" flat tile style="border-bottom: 1px solid #f5f5f5;">
                <v-card-title>
                    <h5 class="font-weight-light">DANH MỤC</h5>
                </v-card-title>
            </v-card>
            <v-card class="grid" rounded="sm" tile flat style="overflow-x: auto;" >
                <v-sheet color="transparent d-flex flex-wrap" max-height="312px" width="142%"> 
                    <v-card tile class="d-flex flex-wrap align-center overflow-x-auto" color="transparent">
                        <v-hover v-for="(category, index) in categories" :key="index" v-slot="{ hover }" >
                            <v-card :elevation="hover ? 2 : 0" class="d-flex flex-column align-center" max-width="119px" height="150px" style="padding: 18px;">
                                <a href="" class="text-decoration-none black--text text-center d-flex flex-column align-center" style="text-wrap: wrap; width: 100px">
                                    <v-img
                                        :src="category.src"
                                        max-width="83px"
                                        max-height="83px"
                                        contain
                                    >

                                    </v-img>
                                
                                    <span class="text-center caption"> {{ category.name }}</span>
                                </a>
                            </v-card>
                        </v-hover>
                    </v-card>
                </v-sheet>
            </v-card>
        </v-sheet>
    </v-sheet>
</template>

<script>
export default {
    name: 'productBody',
    data() {
        return {
            e1: 0,
            steps: [
                { src: "https://cf.shopee.vn/file/vn-11134258-7ras8-m0sil68ehi1b66_xxhdpi" }, 
                { src: "https://cf.shopee.vn/file/sg-11134258-7rdvo-m188y9zt1t8x76_xxhdpi" }, 
                { src: "https://cf.shopee.vn/file/vn-11134258-7ras8-m188wmt5mcmz6f_xxhdpi" }, 
                { src: "https://cf.shopee.vn/file/sg-11134258-7rdwu-m184vwqhxl3t1b_xxhdpi" },
                { src: "https://cf.shopee.vn/file/sg-11134258-7rdvf-m1c5ja9uti1hbb_xxhdpi" },
                { src: "https://cf.shopee.vn/file/sg-11134258-7rdwp-m1cdx5jpvojpa6_xxhdpi" },
                { src: "https://cf.shopee.vn/file/sg-11134258-7rdvt-m1c5jhuvpyka1a_xxhdpi" },
                { src: "https://cf.shopee.vn/file/sg-11134258-7rdvh-m185k7i5tcjyc3_xxhdpi" },
                { src: "https://cf.shopee.vn/file/sg-11134258-7rdyx-m1857c6xw68ubc_xxhdpi" },
                { src: "https://cf.shopee.vn/file/sg-11134258-7rdwy-m1858r0tgyw47d_xxhdpi" },
                { src: "https://cf.shopee.vn/file/sg-11134258-7rdwi-m185dqiyqzkue1_xxhdpi" },
                { src: "https://cf.shopee.vn/file/sg-11134258-7rdxc-m185k56nad9a92_xxhdpi" },
                { src: "https://cf.shopee.vn/file/sg-11134258-7rdxd-m185k3m1iec9cc_xxhdpi" },
                { src: "https://cf.shopee.vn/file/sg-11134258-7rdw7-m186mosslplf08_xxhdpi" },
                { src: "https://cf.shopee.vn/file/sg-11134258-7rdxb-m1894lontabk44_xxhdpi" },
                { src: "https://cf.shopee.vn/file/sg-11134258-7rdyk-m186t36hibd6ca_xxhdpi" },
            ],
            services: [
                { name: "Voucher Giảm Đến 1 Triệu", src: "https://cf.shopee.vn/file/vn-50009109-f6c34d719c3e4d33857371458e7a7059_xhdpi"},
                { name: "Miễn Hết Phí Ship Cho Mọi Đơn", src: "https://cf.shopee.vn/file/a8d76bca057ba0b117dcf8e1ef068d16_xhdpi" },
                { name: "Shopee Siêu Rẻ", src: "https://cf.shopee.vn/file/vn-50009109-91399a1d3ed283d272b069fac5ca989c_xhdpi"},
                { name: "Shopee Style Voucher 30%", src: "https://cf.shopee.vn/file/vn-50009109-c02353c969d19918c53deaa4ea15bdbe_xhdpi"},
                { name: "Hàng Quốc Tế", src: "https://cf.shopee.vn/file/a08ab28962514a626195ef0415411585_xhdpi"},
                { name: "Nạp Thẻ, Dịch Vụ & Vé Phim", src: "https://cf.shopee.vn/file/9df57ba80ca225e67c08a8a0d8cc7b85_xhdpi"},
                { name: "Mã Giảm Giá", src: "https://cf.shopee.vn/file/vn-50009109-8a387d78a7ad954ec489d3ef9abd60b4_xhdpi"},
            ],
            categories: [
                { name: 'Thời Trang Nam', src: "https://down-vn.img.susercontent.com/file/687f3967b7c2fe6a134a2c11894eea4b" },
                { name: 'Điện Thoại & Phụ Kiện', src: "https://down-vn.img.susercontent.com/file/31234a27876fb89cd522d7e3db1ba5ca" },
                { name: 'Thiết Bị Điện Tử', src: "https://down-vn.img.susercontent.com/file/978b9e4cb61c611aaaf58664fae133c5" },
                { name: 'Máy Tính & Laptop', src: "https://down-vn.img.susercontent.com/file/c3f3edfaa9f6dafc4825b77d8449999d" },
                { name: 'Máy Ảnh & Máy Quay Phim', src: "https://down-vn.img.susercontent.com/file/ec14dd4fc238e676e43be2a911414d4d" },
                { name: 'Đồng Hồ', src: "https://down-vn.img.susercontent.com/file/86c294aae72ca1db5f541790f7796260" },
                { name: 'Giày Dép Nam', src: "https://down-vn.img.susercontent.com/file/74ca517e1fa74dc4d974e5d03c3139de" },
                { name: 'Thiết Bị Điện Gia Dụng', src: "https://down-vn.img.susercontent.com/file/7abfbfee3c4844652b4a8245e473d857" },
                { name: 'Thể Thao & Du Lịch', src: "https://down-vn.img.susercontent.com/file/6cb7e633f8b63757463b676bd19a50e4" },
                { name: 'Ô Tô & Xe Máy & Xe Đạp', src: "https://down-vn.img.susercontent.com/file/3fb459e3449905545701b418e8220334" },
                { name: 'Balo & Túi Ví Nam', src: "https://down-vn.img.susercontent.com/file/18fd9d878ad946db2f1bf4e33760c86f" },
                { name: 'Đồ Chơi', src: "https://down-vn.img.susercontent.com/file/ce8f8abc726cafff671d0e5311caa684" },
                { name: 'Chăm Sóc Thú Cưng', src: "https://down-vn.img.susercontent.com/file/cdf21b1bf4bfff257efe29054ecea1ec" },
                { name: 'Dụng cụ và thiết bị tiện ích', src: "https://down-vn.img.susercontent.com/file/e4fbccba5e1189d1141b9d6188af79c0" },
                { name: 'Thời Trang Nữ', src: "https://down-vn.img.susercontent.com/file/75ea42f9eca124e9cb3cde744c060e4d" },
                { name: 'Mẹ & Bé', src: "https://down-vn.img.susercontent.com/file/099edde1ab31df35bc255912bab54a5e" },
                { name: 'Nhà Cửa & Đời Sống', src: "https://down-vn.img.susercontent.com/file/24b194a695ea59d384768b7b471d563f" },
                { name: 'Sắc Đẹp', src: "https://down-vn.img.susercontent.com/file/ef1f336ecc6f97b790d5aae9916dcb72" },
                { name: 'Sức Khỏe', src: "https://down-vn.img.susercontent.com/file/49119e891a44fa135f5f6f5fd4cfc747" },
                { name: 'Giày Dép Nữ', src: "https://down-vn.img.susercontent.com/file/48630b7c76a7b62bc070c9e227097847" },
                { name: 'Túi Ví Nữ', src: "https://down-vn.img.susercontent.com/file/fa6ada2555e8e51f369718bbc92ccc52" },
                { name: 'Phụ Kiện & Trang Sức Nữ', src: "https://down-vn.img.susercontent.com/file/8e71245b9659ea72c1b4e737be5cf42e" },
                { name: 'Bách Hóa Online', src: "https://down-vn.img.susercontent.com/file/c432168ee788f903f1ea024487f2c889" },
                { name: 'Nhà Sách Online', src: "https://down-vn.img.susercontent.com/file/36013311815c55d303b0e6c62d6a8139" },
                { name: 'Thời Trang Trẻ Em', src: "https://down-vn.img.susercontent.com/file/4540f87aa3cbe99db739f9e8dd2cdaf0" },
                { name: 'Giặt Giũ & Chăm Sóc Nhà Cửa', src: "https://down-vn.img.susercontent.com/file/cd8e0d2e6c14c4904058ae20821d0763" },
                { name: 'Voucher & Dịch Vụ', src: "https://down-vn.img.susercontent.com/file/b0f78c3136d2d78d49af71dd1c3f38c1" },
            ],
        }
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

.v-list-item__title, .v-list-item__subtitle {
    overflow: visible !important;
}

.v-list-item__content {
    flex: none;
    align-self: normal;
    padding: 6px 0;
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

::v-deep .v-icon.notranslate.mdi.mdi-circle.theme--dark {
    font-size: 10px !important;
    
}

::v-deep .v-carousel__controls__item.v-btn.v-btn--icon.v-btn--round.theme--dark.v-size--small {
    width: 6px !important;
    height: 6px !important;

}

::v-deep .v-window__prev{
    border-radius: 0;
    background-color: rgba(0, 0, 0, 0.8);
}

::v-deep .v-window__next {
    border-radius: 0;
    background-color: rgba(0, 0, 0, 0.8);
}

::v-deep .v-carousel__controls__item.v-btn.v-item--active.v-btn--icon.v-btn--round.theme--dark.v-size--small {
    color: #ff2600;
    width: 10px;
    height: 10px;
    opacity: 1;
}



</style>