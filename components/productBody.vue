<template>
    <v-sheet color="white" style="margin-top: 120px">
        <div class="grid">
            <div class="d-flex pt-7 pb-3 flex-column" >
                <v-sheet class="flex-grow-1 d-flex" color="transparent" max-width="100%">
                    <!-- Product Advertisements -->
                    <v-stepper  class="flex-grow-1" non-linear rounded="2" flat height="100%" v-model="e1">
                        <v-stepper-header class="justify-center align-end" style="height: 100%;">
                            <v-hover v-slot="{ hover }">
                                <v-stepper-items
                                    class="d-flex align-end justify-center" 
                                    height="100%" 
                                    style="position:relative; overflow: hidden;"
                                    tile
                                >
                                    <div>
                                        <v-stepper-content v-for="(step, index) in steps" :key="index" :step="index" class="pa-0" >
                                            <v-img :src="step.src" width="796px" height="235px" ></v-img>
                                        </v-stepper-content>
                                    </div>
                                    
                                    <div style="position:absolute;" class="d-flex mb-4">
                                        <v-stepper-step 
                                            v-for="(step, index) in steps" 
                                            :key="index" 
                                            editable 
                                            :step="index"
                                        >
                                        </v-stepper-step>
                                    </div>

                                    <div>
                                        <v-fade-transition>
                                            <v-btn
                                                v-if="hover" 
                                                @click="e1 = e1 > 0 ? e1 - 1 : steps.length - 1"
                                                absolute
                                                style="top: calc(40% - 5px); left: 0;"
                                                height="60px"
                                                class="pa-0 white--text"
                                                min-width="35px"
                                                color="#00000052"
                                                tile
                                            >
                                                <v-icon>mdi-chevron-left</v-icon>
                                            </v-btn>
                                        </v-fade-transition>
                                        <v-fade-transition>
                                            <v-btn
                                                v-if="hover" 
                                                @click="e1 = (e1 + 1) % steps.length || 0"
                                                absolute
                                                style="top: calc(40% - 5px); right: 0;"
                                                height="60px"
                                                width="35px"
                                                class="pa-0 white--text"
                                                min-width="35px"
                                                color="#00000052"
                                                tile
                                            >
                                                <v-icon>mdi-chevron-right</v-icon>
                                            </v-btn>
                                        </v-fade-transition>
                                    </div>
                                </v-stepper-items>
                            </v-hover>
                        </v-stepper-header>
                    </v-stepper>
                    
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

                <v-sheet>
                    <!-- Product Services -->
                    <v-list class="pa-0 col-12">
                        <v-list-item class="pa-0 col-12">
                            <v-list-item-content class="d-flex justify-space-around col-12 pt-2">
                                <v-list-item-title class="d-flex justify-center align-center col-2 pa-0" v-for="(service, index) in services" :key="index" style="width: auto;">
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

        <v-sheet color="grey pt-5">
            <v-card class="grid" rounded="sm" flat max-height="302px">
                <v-card-title>
                    <h4>DANH MỤC</h4>
                </v-card-title>
                <v-list class="pa-0 d-flex">
                    <v-list-item class="pa-0 d-flex col overflow-x-auto">
                        <v-list-content v-for="(category, index) in categories" :key="index" class="col-2">
                            <a href="" class="text-decoration-none black--text">
                                <div class="d-flex flex-column align-center">
                                    <v-img
                                        :src="category.src"
                                        height="83px"
                                        max-width="85px"
                                        contain
                                        position="center"
                                    ></v-img>
                                    <v-list-item-title class="subtitle-2">{{ category.name }}</v-list-item-title>
                                </div>                                
                            </a>
                        </v-list-content>
                    </v-list-item>
                </v-list>
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
            ],
            categories: [
                { name: 'Thời Trang Nam', src: "https://down-vn.img.susercontent.com/file/687f3967b7c2fe6a134a2c11894eea4b" },
                { name: 'Thời Trang Nam', src: "https://down-vn.img.susercontent.com/file/687f3967b7c2fe6a134a2c11894eea4b" },
                { name: 'Thời Trang Nam', src: "https://down-vn.img.susercontent.com/file/687f3967b7c2fe6a134a2c11894eea4b" },
                { name: 'Thời Trang Nam', src: "https://down-vn.img.susercontent.com/file/687f3967b7c2fe6a134a2c11894eea4b" },
                { name: 'Thời Trang Nam', src: "https://down-vn.img.susercontent.com/file/687f3967b7c2fe6a134a2c11894eea4b" },
                { name: 'Thời Trang Nam', src: "https://down-vn.img.susercontent.com/file/687f3967b7c2fe6a134a2c11894eea4b" },
                { name: 'Thời Trang Nam', src: "https://down-vn.img.susercontent.com/file/687f3967b7c2fe6a134a2c11894eea4b" },
                { name: 'Thời Trang Nam', src: "https://down-vn.img.susercontent.com/file/687f3967b7c2fe6a134a2c11894eea4b" },
                { name: 'Thời Trang Nam', src: "https://down-vn.img.susercontent.com/file/687f3967b7c2fe6a134a2c11894eea4b" },
                { name: 'Thời Trang Nam', src: "https://down-vn.img.susercontent.com/file/687f3967b7c2fe6a134a2c11894eea4b" },
                { name: 'Thời Trang Nam', src: "https://down-vn.img.susercontent.com/file/687f3967b7c2fe6a134a2c11894eea4b" },
                { name: 'Thời Trang Nam', src: "https://down-vn.img.susercontent.com/file/687f3967b7c2fe6a134a2c11894eea4b" },
                { name: 'Thời Trang Nam', src: "https://down-vn.img.susercontent.com/file/687f3967b7c2fe6a134a2c11894eea4b" },
                { name: 'Thời Trang Nam', src: "https://down-vn.img.susercontent.com/file/687f3967b7c2fe6a134a2c11894eea4b" },
                { name: 'Thời Trang Nữ', src: "https://down-vn.img.susercontent.com/file/687f3967b7c2fe6a134a2c11894eea4b" },
            ]
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

.v-stepper__step {
    padding: 0;
    background-color: rgb(255, 255, 255, 0.6);
    width: 10px;
    height: 10px;
    border-radius: 50%;
    border: 1px solid #ccc;
    margin: 0 5px;
}

span.v-stepper__step__step,
.v-application--is-ltr .v-stepper__step__step {
    margin: 0;
}

::v-deep span.v-stepper__step__step {
    display: none;
}

</style>