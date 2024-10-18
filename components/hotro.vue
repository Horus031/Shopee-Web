<template>
    <div class="d-flex" style="justify-content: center; display: flex; flex-direction: column;">
        <v-card style="background-color: #ee4d2d ; display: flex; flex-direction: column; align-items: center;" class="real" elevation="0" outlined>
            <v-card-title class="pa-0 ma-0 d-flex flex-column" style="padding:0px; justify-content: center;">
                <p style="color: white; padding-bottom: 38px;padding-top: 60px; font-size: 36px; text-align: center; font-weight: normal;">Xin chào, Shopee có thể giúp gì cho bạn?</p>
            </v-card-title>
            <v-form style="width: 796px; position: relative; display: flex; padding: 2px;">
                    <v-text-field solo flat placeholder="Nhập từ khoá hoặc nội dung cần tìm" class="searchbar" style="margin:auto ; padding-bottom: 10px; flex: 1;">
                    </v-text-field> 
                    <v-btn color="#ee4d2d" height="52px" width="80px" absolute style="right: 4px; top: 4px" depressed>
                                <v-icon style="color: white;" large>mdi mdi-magnify</v-icon>
                    </v-btn>
            </v-form>  
        </v-card>
        <v-sheet style="margin: auto;" class="cont">
            <p class="supersmall font" style=" max-width:130px; min-width: 130px;margin-top:5%  ; margin-bottom: 2%;">
                Danh mục
            </p>
            <div class="flexbig">
                <v-card class="card flex" elevation="0" outlined>
                    <img class="img" src="https://cs.deo.shopeemobile.com/shopee/shopee-cs-live-sg/static/helpcenterfe/hc-category-icons/690d84d4103544139d22ba177c6dca97.png">
                    <v-card-title class="smallfont">Mua Sắm Cùng Shopee</v-card-title>
                </v-card>
                <v-card class="card flex" elevation="0" outlined>
                    <img class="img" src="https://cs.deo.shopeemobile.com/shopee/shopee-cs-live-sg/static/helpcenterfe/hc-category-icons/c2fb3ede3472487c82131982f5ab8cbf.png">
                    <v-card-title class="smallfont">Khuyến Mãi & Ưu Đãi</v-card-title>
                </v-card>
                <v-card class="card flex" elevation="0" outlined>
                    <img style="margin-left: 12px; margin-right: 12px; margin-top: auto;margin-bottom: auto;" src="https://cs.deo.shopeemobile.com/shopee/shopee-cs-live-sg/static/helpcenterfe/hc-category-icons/a7c785163abc4abcbeeaefcb5bc54cc1.png">
                    <v-card-title class="smallfont">Thanh toán</v-card-title>
                </v-card>
                <v-card class="card flex" elevation="0" outlined>
                    <img class="img" src="https://cs.deo.shopeemobile.com/shopee/shopee-cs-live-sg/static/helpcenterfe/hc-category-icons/a0747397630545a7ae270dadfe73ecf5.png">
                    <v-card-title class="smallfont">Đơn Hàng & Vận Chuyển</v-card-title>
                </v-card>
            </div>
            <div class="flexbig" style="margin-top: 20px;">
                <v-card class="card flex" elevation="0" outlined>
                    <img class="img" src="https://cs.deo.shopeemobile.com/shopee/shopee-cs-live-sg/static/helpcenterfe/hc-category-icons/f2bc745edbfd4d7095d87da7dade354a.png">
                    <v-card-title class="smallfont">Trả Hàng & Hoàn Tiền</v-card-title>
                </v-card>
                <v-card class="card flex" elevation="0" outlined>
                    <img class="img" src="https://cs.deo.shopeemobile.com/shopee/shopee-cs-live-sg/static/helpcenterfe/hc-category-icons/83c742e5e2cb4f108ea4ee942aa68af2.png">
                    <v-card-title class="smallfont">Thông Tin Chung</v-card-title>
                </v-card>
                <div class="card"></div>
                <div class="card"></div>
            </div>
            <p class="supersmall font" style="margin-top: 30px; margin-bottom: 20px;">
                Câu Hỏi Thường Gặp
            </p>
            <v-list>
                <v-list-item>
                    <v-list-item-content style="padding: 0px;">
                    <v-list-item-title class="question" style="border-top: 1px dashed #e1e1e1;;">[Cảnh báo lừa đảo] Mua sắm an toàn cùng Shopee</v-list-item-title>
                    </v-list-item-content>
                </v-list-item>
                

                
                <v-list-item>
                    <v-list-item-content style="padding: 0px;">
                    <v-list-item-title class="question">[Dịch vụ] Cách liên hệ Chăm sóc khách hàng, Hotline, Tổng đài Shopee</v-list-item-title>
                    </v-list-item-content>
                </v-list-item>
                

            </v-list>
        </v-sheet>
    </div>
</template>

<script>
</script>
<style scoped>
::v-deep .icon-margin .v-icon {
  margin:10px /* Add margin here */
}
.img{
    margin:auto;
}
.smallfont{
    font-weight: 300;
    font-size: 17px;
}
.card{
    min-width: 279px;
    max-width: 279px;
    min-height: 80px;
}
.flexbig{
    display: flex;
    justify-content: space-between;
}
.flex{
    display: flex;
}

.font{
    font-size: 24px;
    font-weight: 500;
    line-height: 24px;
    font-family: Roboto, system-ui, -apple-system, BlinkMacSystemFont, PingFang SC, Source Han Sans CN-Normal, Noto Sans CJK SC, Segoe UI, Helvetica Neue, Helvetica, Hiragino Sans GB, Microsoft YaHei, Arial, sans-serif;
}

.real{
    
    font-family: Roboto, system-ui, -apple-system, BlinkMacSystemFont, PingFang SC, Source Han Sans CN-Normal, Noto Sans CJK SC, Segoe UI, Helvetica Neue, Helvetica, Hiragino Sans GB, Microsoft YaHei, Arial, sans-serif;
}
.cont{
    width: 1000px;
    max-width: 100%;
    margin: 0 auto;
    font-family: Roboto, system-ui, -apple-system, BlinkMacSystemFont, PingFang SC, Source Han Sans CN-Normal, Noto Sans CJK SC, Segoe UI, Helvetica Neue, Helvetica, Hiragino Sans GB, Microsoft YaHei, Arial, sans-serif;

}
.gg{
    max-width: 81%;
    min-width: 81%;
    font-size: 20px;
    font-weight: 400;
    line-height: 59px;
    font-family: Roboto, system-ui, -apple-system, BlinkMacSystemFont, PingFang SC, Source Han Sans CN-Normal, Noto Sans CJK SC, Segoe UI, Helvetica Neue, Helvetica, Hiragino Sans GB, Microsoft YaHei, Arial, sans-serif;
}

.supersmall{
    min-width: 350px;
    max-width: 350px;
}
.question{
    padding: 16px 10px;
    font-size: 18px;
    line-height: 28px;
    cursor: pointer;
    border-bottom: 1px dashed #e1e1e1;
}

::v-deep .v-input__slot {
    height: 56px;
}

::v-deep .v-text-field input {
    font-size: 20px;
    padding: 0 10px;
}

</style>
