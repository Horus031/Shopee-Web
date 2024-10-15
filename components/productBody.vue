<template>
    <v-sheet color="white" style="margin-top: 120px">
        <div class="grid">
            <div class="d-flex pt-7 pb-7" >
                <v-sheet class="flex-grow-1" color="transparent" max-width="800px">
                    <v-stepper non-linear rounded="2" flat height="100%" v-model="e1">
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
                </v-sheet>

                <v-sheet class="d-flex flex-column justify-space-between" color="transparent">
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
            </div>
        </div>
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
        }
    },
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