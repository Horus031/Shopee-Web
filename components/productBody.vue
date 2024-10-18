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

        <v-sheet color="grey pt-5" >
            <v-card class="grid" rounded="sm" flat>
                <v-card-title>
                    <h5>DANH MỤC</h5>
                </v-card-title>
                <v-sheet color="transparent overflow-x-auto d-flex flex-wrap justify-space-between">
                    <v-hover v-for="(category, index) in categories" :key="index" v-slot="{ hover }" class="pa-4">
                        <v-card :elevation="hover ? 3 : 0" tile class="d-flex flex-column align-center" max-width="120px" color="transparent">
                            <v-img
                            :src="category.src"
                            max-width="83px"
                            max-height="83px"
                            contain
                        >

                            </v-img>
                            
                            <span class="text-center caption" style="text-wrap: wrap;"> {{ category.name }}</span>
                        </v-card>
                    </v-hover>
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
                { name: 'Máy Ảnh & Máy Quay Phim', src: "https://down-vn.img.susercontent.com/file/687f3967b7c2fe6a134a2c11894eea4b" },
                { name: 'Đồng Hồ', src: "https://down-vn.img.susercontent.com/file/687f3967b7c2fe6a134a2c11894eea4b" },
                { name: 'Giày Dép Nam', src: "https://down-vn.img.susercontent.com/file/687f3967b7c2fe6a134a2c11894eea4b" },
                { name: 'Thiết Bị Điện Gia Dụng', src: "https://down-vn.img.susercontent.com/file/687f3967b7c2fe6a134a2c11894eea4b" },
                { name: 'Thể Thao & Du Lịch', src: "https://down-vn.img.susercontent.com/file/687f3967b7c2fe6a134a2c11894eea4b" },
                { name: 'Ô Tô & Xe Máy & Xe Đạp', src: "https://down-vn.img.susercontent.com/file/687f3967b7c2fe6a134a2c11894eea4b" },
                { name: 'Thời Trang Nữ', src: "https://down-vn.img.susercontent.com/file/687f3967b7c2fe6a134a2c11894eea4b" },
                { name: 'Mẹ & Bé', src: "https://down-vn.img.susercontent.com/file/687f3967b7c2fe6a134a2c11894eea4b" },
                { name: 'Nhà Cửa & Đời Sống', src: "https://down-vn.img.susercontent.com/file/687f3967b7c2fe6a134a2c11894eea4b" },
                { name: 'Sắc Đẹp', src: "https://down-vn.img.susercontent.com/file/687f3967b7c2fe6a134a2c11894eea4b" },
                { name: 'Sức Khỏe', src: "https://down-vn.img.susercontent.com/file/687f3967b7c2fe6a134a2c11894eea4b" },
                { name: 'Giày Dép Nữ', src: "https://down-vn.img.susercontent.com/file/687f3967b7c2fe6a134a2c11894eea4b" },
                { name: 'Túi Ví Nữ', src: "https://down-vn.img.susercontent.com/file/687f3967b7c2fe6a134a2c11894eea4b" },
                { name: 'Phụ Kiện & Trang Sức Nữ', src: "https://down-vn.img.susercontent.com/file/687f3967b7c2fe6a134a2c11894eea4b" },
                { name: 'Bách Hóa Online', src: "https://down-vn.img.susercontent.com/file/687f3967b7c2fe6a134a2c11894eea4b" },
                { name: 'Nhà Sách Online', src: "https://down-vn.img.susercontent.com/file/687f3967b7c2fe6a134a2c11894eea4b" },
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