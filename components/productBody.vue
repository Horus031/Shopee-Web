<template>
    <v-sheet color="white" style="margin-top: 120px">
        <div class="grid">
            <div class="d-flex pt-7 pb-7" >
                <v-sheet class="flex-grow-1" color="transparent" max-width="800px">
                    <v-stepper non-linear rounded="2" flat height="100%" v-model="e1">
                        <v-stepper-header class="justify-center align-end" style="height: 100%;">
                            <v-card 
                                class="d-flex align-end justify-center" 
                                height="100%" 
                                style="position:relative"
                                rounded="sm"
                            >
                                <div>
                                    <v-stepper-content v-for="(step, index) in steps" :key="index" :step="index + 1" class="pa-0">
                                        <v-img :src="step.src" width="796px" height="240px"></v-img>
                                    </v-stepper-content>
                                </div>
                                
                                <div style="position:absolute;" class="d-flex mb-4">
                                    <v-stepper-step 
                                        v-for="(step, index) in steps" 
                                        :key="index" 
                                        editable 
                                        :step="index + 1"
                                    >
                                    </v-stepper-step>
                                </div>
                            </v-card>
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
            e1: 1,
            steps: [
                { src: "https://cf.shopee.vn/file/vn-11134258-7ras8-m188wmt5mcmz6f_xxhdpi" },
                { src: "https://cf.shopee.vn/file/vn-11134258-7ras8-m188wmt5mcmz6f_xxhdpi" },
                { src: "https://cf.shopee.vn/file/vn-11134258-7ras8-m188wmt5mcmz6f_xxhdpi" },
                { src: 'https://cf.shopee.vn/file/sg-11134258-7rdvy-m16q7tvpi2fi29_xxhdpi' },
                { src: 'https://cf.shopee.vn/file/sg-11134258-7rdvy-m16q7tvpi2fi29_xxhdpi' },
                { src: 'https://cf.shopee.vn/file/sg-11134258-7rdvy-m16q7tvpi2fi29_xxhdpi' },
                { src: 'https://cf.shopee.vn/file/sg-11134258-7rdvy-m16q7tvpi2fi29_xxhdpi' },
                { src: 'https://cf.shopee.vn/file/sg-11134258-7rdvy-m16q7tvpi2fi29_xxhdpi' },
                { src: 'https://cf.shopee.vn/file/sg-11134258-7rdvy-m16q7tvpi2fi29_xxhdpi' },
                { src: 'https://cf.shopee.vn/file/sg-11134258-7rdvy-m16q7tvpi2fi29_xxhdpi' },
                { src: 'https://cf.shopee.vn/file/sg-11134258-7rdvy-m16q7tvpi2fi29_xxhdpi' },
                { src: 'https://cf.shopee.vn/file/sg-11134258-7rdvy-m16q7tvpi2fi29_xxhdpi' },
                { src: 'https://cf.shopee.vn/file/sg-11134258-7rdvy-m16q7tvpi2fi29_xxhdpi' },
                { src: 'https://cf.shopee.vn/file/sg-11134258-7rdvy-m16q7tvpi2fi29_xxhdpi' },
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