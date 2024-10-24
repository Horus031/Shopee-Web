<template>
    <div class="grid pt-4">
        <v-dialog
            v-model="dialog"
            width="600"
            class="d-flex justify-center"
            style="box-shadow: none;"
        >
            <template v-slot:activator="{ on, attrs }">
                <a v-bind="attrs" v-on="on">
                    <v-img
                        src="https://cf.shopee.vn/file/vn-11134258-7r98o-lylx97r9vezl4e"
                        width="100%"
                        height="120px"
                        contain
                        position="center"
                    >
                    </v-img>
                </a>
            </template>

            <div class="ma-6" style="position: relative">
                <v-card class="d-flex pa-8" rounded="sm" flat>
                    <v-sheet class="col-9 pa-0 d-flex flex-column" color="transparent">
                        <div>
                            <v-card-title class="pa-0 col-11" style="font-size: 22px; line-height: 1.2;">
                                Tải ứng dụng Shopee để nhận ngay Quà Tặng từ chúng tớ nhé!
                            </v-card-title>
                            
                            <v-card-text class="pa-0 mt-2 mb-7 col-11" style="font-size: 18px;">
                                Nhận quà tặng và các deal độc quyền ngay bây giờ.
                            </v-card-text>
                            
                            <v-sheet 
                                color="transparent" 
                                class="d-flex align-center col-11 pa-0"
                                max-height="51px"
                            >
                                <div class="pt-1 mr-2">
                                    <a href="http://app.appsflyer.com/959841449?pid=web_referral" target="_blank">
                                        <v-img
                                            class="d-flex mr-2"
                                            :src="require('@/assets/img/appstore_qrcode.png')"
                                            max-height="51px"
                                            max-width="154px"
                                            position="center"
                                            contain
                                        >
                                        </v-img>
                                    </a>
                                </div>
                                <div class="pt-1 mr-2">
                                    <a href="http://app.appsflyer.com/com.shopee.vn?pid=web_referral" target="_blank">
                                        <v-img
                                            class="d-flex"
                                            :src="require('@/assets/img/googleplay_qrcode.png')"
                                            max-height="51px"
                                            max-width="154px"
                                            position="center"
                                            contain
                                        >
                                        </v-img>
                                    </a>
                                </div>
                            </v-sheet>
                        </div>
                        
                    </v-sheet>

                    <div class="col-3 pa-0">
                        <v-img
                            src="https://deo.shopeemobile.com/shopee/shopee-pcmall-live-sg/assets/5b6e787c2e5ee052.png"
                            height="100%"
                            contain
                            position="center"
                        >
                        </v-img>

                        
                    </div>

                    
                </v-card>
                <v-btn
                    class="freeAds__btn"    
                    icon
                    rounded
                    absolute
                    height="30px"
                    width="30px"
                    @click="dialog = false"
                >
                    <v-icon 
                        color="white" 
                        small
                        style="font-size: 20px;"
                        
                    >
                        mdi mdi-close
                    </v-icon>
                </v-btn>
            </div>
            
        </v-dialog>
    </div>
</template>

<script>
export default {
    name: 'bodyFreeAds',
    data() {
        return {
            dialog: false,
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

.freeAds__btn {
    border: 3px solid white; 
    top: -11px; 
    right: -9px; 
    background-color: #5a5a5a;
}

::v-deep div.v-dialog.v-dialog--active {
    display: flex;
    justify-content: center;
    box-shadow: none;
    overflow: hidden;
}

</style>