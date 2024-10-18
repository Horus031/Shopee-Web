<template>
    <div class="cont d-flex" style="justify-content: center; display: flex; flex-direction: column;">
        <v-card style="background-color: #ee4d2d ; display: flex;flex-direction: column;" class="real" elevation="0" outlined>
            <v-card-title class="pa-0 ma-0" style="padding:0px; justify-content: center;">
                <div style="min-width:700px; max-width: 700px;">
                    <p style="color: white; padding-bottom: 50px;padding-top: 25px; font-size: 36px; text-align: center;">Xin chào shopee có thể giúp gì cho bạn?</p>
                    <v-text-field outlined solo placeholder="nhập từ khoá hoặc nội dung cần tìm" label="nhập từ khoá hoặc nội dung cần tìm" class="searchbar" style="margin:auto ; padding-bottom: 10px; position: relative; ">
                        
                    </v-text-field> 
                </div>
            </v-card-title>    
        </v-card>
        <v-sheet class="small" style="margin: auto;">
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
.searchbar{
    min-width: 550px;
}
.font{
    font-size: 24px;
    font-weight: 500;
    line-height: 24px;
    font-family: Roboto, system-ui, -apple-system, BlinkMacSystemFont, PingFang SC, Source Han Sans CN-Normal, Noto Sans CJK SC, Segoe UI, Helvetica Neue, Helvetica, Hiragino Sans GB, Microsoft YaHei, Arial, sans-serif;
}

.real{
    min-width: 1530px;
    max-width: 1530px;
    font-family: Roboto, system-ui, -apple-system, BlinkMacSystemFont, PingFang SC, Source Han Sans CN-Normal, Noto Sans CJK SC, Segoe UI, Helvetica Neue, Helvetica, Hiragino Sans GB, Microsoft YaHei, Arial, sans-serif;
}
.cont{
    min-width: 1530px;
    max-width: 1530px;
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
.small{
    min-width: 81%;
    max-width: 81%;
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
</style>
