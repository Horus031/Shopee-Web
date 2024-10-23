<template>
    <div>
        <v-sheet color="white" style="margin-top: 120px" elevation="2">
            <div class="grid">
                <div class="d-flex pt-7 pb-3 flex-column" >
                    <v-sheet class="flex-grow-1 d-flex" color="transparent" max-width="100%">
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
                                                <div style="line-height: 1; font-size: 14px; width: 60%;">
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
        </v-sheet>
    </div>
</template>

<script>
export default {
    name: 'bodyProductAds',
    data () {
        return {
            steps: [ // Advertisements for customers
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
            services: [ // Service for customers
                {   name: "Voucher Giảm Đến 1 Triệu", 
                    src: "https://cf.shopee.vn/file/vn-50009109-f6c34d719c3e4d33857371458e7a7059_xhdpi"
                },
                {   name: "Miễn Phí Ship - Có Shopee",
                    src: "https://cf.shopee.vn/file/vn-50009109-c7a2e1ae720f9704f92f72c9ef1a494a_xhdpi" 
                },
                {   name: "Khung Giờ Săn Sale", 
                    src: "https://cf.shopee.vn/file/e4a404283b3824c211c1549aedd28d5f_xhdpi"
                },
                {   name: "Mã Giảm Giá", 
                    src: "https://cf.shopee.vn/file/vn-50009109-8a387d78a7ad954ec489d3ef9abd60b4_xhdpi"
                },
                {   name: "Shopee Siêu Rẻ", 
                    src: "https://cf.shopee.vn/file/vn-50009109-91399a1d3ed283d272b069fac5ca989c_xhdpi"
                },
                {   name: "Shopee Style Voucher 30%", 
                    src: "https://cf.shopee.vn/file/vn-50009109-c02353c969d19918c53deaa4ea15bdbe_xhdpi"
                },
                {   name: "Quốc Tế Siêu Trợ Giá", 
                    src: "https://cf.shopee.vn/file/vn-11134258-7ras8-m0vja5rfwyvj10_xhdpi"
                },
                {   name: "Nạp Thẻ, Dịch Vụ & Vé Phim", 
                    src: "https://cf.shopee.vn/file/9df57ba80ca225e67c08a8a0d8cc7b85_xhdpi"
                },
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