<template>
    <v-sheet color="grey lighten-4 pt-5">
        <div class="grid">
            <v-dialog
                v-model="dialog"
                width="600"
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

                <v-card class="d-flex pa-8">
                    <div class="col-8">
                        <v-card-title class="pa-0" style="font-size: 22px">
                            Tải ứng dụng Shopee để nhận ngay Quà Tặng từ chúng tớ nhé!
                        </v-card-title>

                        <v-card-text class="pa-0" style="font-size: 20px;">
                            Nhận quà tặng và các deal độc quyền ngay bây giờ.
                        </v-card-text>
                    </div>

                    <div class="col-4">
                        <v-img
                            src="https://deo.shopeemobile.com/shopee/shopee-pcmall-live-sg/assets/5b6e787c2e5ee052.png"
                            height="80px"
                            contain
                            position="center"
                        >
                        </v-img>

                        <v-sheet 
                            color="transparent" 
                            class="d-flex justify-space-between flex-wrap" 
                            style="padding: 0 15px 5px 15px;"
                        >
                            <div class="pt-1">
                                <v-img
                                    class="d-flex"
                                    :src="require('@/assets/img/appstore_qrcode.png')"
                                    height="18px"
                                    width="70px"
                                    position="left center"
                                    contain
                                >
                                </v-img>
                            </div>
                            <div class="pt-1">
                                <v-img
                                    class="d-flex"
                                    :src="require('@/assets/img/googleplay_qrcode.png')"
                                    height="18px"
                                    width="70px"
                                    position="left center"
                                    contain
                                >
                                </v-img>
                            </div>
                        </v-sheet>
                    </div>

                    <v-btn 
                        icon
                        right
                        absolute
                        rounded
                        @click="dialog = false"
                    >
                        <v-icon>mdi mdi-close</v-icon>
                    </v-btn>

                </v-card>
            </v-dialog>
        </div>
    </v-sheet>
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

<style>
.grid {
    width: 1200px;
    max-width: 100%;
    margin: 0 auto;
}

</style>