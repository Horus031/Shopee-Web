<template>
    <div>
        <div class="pa-1">
            <div v-for="(footerCate, index) in footerCategories" :key="index"> 
                <div>
                    <div style="margin: 10px 0 2px 0; padding: 2px 0">
                        <v-hover v-slot="{ hover }">
                            <a
                                :class="hover ? 'shopeecolor--text' : 'grey--text darken-4'"
                                href="" 
                                class="caption text-decoration-none font-weight-bold "
                            >
                                {{ footerCate.name }}
                            </a>
                        </v-hover>
                    </div>
                </div>

                <div class="d-flex flex-wrap mb-2" >
                    <div class="caption">
                        <span class="d-block">
                            <span 
                                v-for="(cate, index) in footerCate.cates" 
                                :key="index" 
                                class="grey--text lighten-2 font-weight-light"
                            >
                                <v-hover v-slot="{ hover }">
                                    <a 
                                        :class="hover ? 'shopeecolor--text' : 'grey--text lighten-2'"
                                        href="" 
                                        class="text-decoration-none "
                                    >
                                        {{ cate.catName }}
                                    </a>
                                </v-hover>
                                <template v-if="index < footerCate.cates.length - 1"> | </template>
                            </span>
                        </span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'footerCategoriesCol1',
    data() {
        return {
            footerCategories: [
                {   name: 'THỜI TRANG NAM', 
                    cates: [
                        { catName: 'Áo Khoác' },
                        { catName: 'Áo Vest và Blazer' },
                        { catName: 'Áo Hoodie, Áo Len & Áo Nỉ' },
                        { catName: 'Quần Jeans' },
                        { catName: 'Quần Dài/Quần Âu' },
                        { catName: 'Quần Short ' },
                        { catName: 'Áo' },
                        { catName: 'Áo Ba Lỗ' },
                        { catName: 'Đồ Lót' },
                        { catName: 'Đồ Ngủ' },
                        { catName: 'Đồ Bộ' },
                        { catName: 'Vớ/Tất' },
                        { catName: 'Trang Phục Truyền Thống' },
                        { catName: 'Đồ Hóa Trang' },
                        { catName: 'Trang Phục Ngành Nghề' },
                        { catName: 'Khác' },
                        { catName: 'Trang Sức Nam' },
                        { catName: 'Kính Mắt Nam' },
                        { catName: 'Thắt Lưng Nam' },
                        { catName: 'Cà vạt & Nơ cổ' },
                        { catName: 'Phụ Kiện Nam' },
                        
                    ]
                },
                {   name: 'NHÀ CỬA & ĐỜI SỐNG', 
                    cates: [
                        { catName: 'Chăn, Ga, Gối & Nệm' },
                        { catName: 'Đồ nội thất' },
                        { catName: 'Trang trí nhà cửa' },
                        { catName: 'Dụng cụ & Thiết bị tiện ích' },
                        { catName: 'Đồ dùng nhà bếp và hộp đựng thực phẩm' },
                        { catName: 'Đèn' },
                        { catName: 'Ngoài trời & Sân vườn' },
                        { catName: 'Đồ dùng phòng tắm' },
                        { catName: 'Vật phẩm thờ cúng' },
                        { catName: 'Đồ trang trí tiệc' },
                        { catName: 'Chăm sóc nhà cửa và giặt ủi' },
                        { catName: 'Sắp xếp nhà cửa' },
                        { catName: 'Dụng cụ pha chế' },
                        { catName: 'Tinh dầu thơm phòng' },
                        { catName: 'Đồ dùng phòng ăn' },
                    ]
                },
                {   name: 'ĐỒNG HỒ', 
                    cates: [
                        { catName: 'Đồng Hồ Nam' },
                        { catName: 'Đồng Hồ Nữ' },
                        { catName: 'Bộ Đồng Hồ & Đồng Hồ Cặp' },
                        { catName: 'Đồng Hồ Trẻ Em' },
                        { catName: 'Phụ Kiện Đồng Hồ' },
                        { catName: 'Khác' },
                    ]
                },
                {   name: 'PHỤ KIỆN & TRANG SỨC NỮ', 
                    cates: [
                        { catName: 'Nhẫn' },
                        { catName: 'Bông tai' },
                        { catName: 'Khăn choàng' },
                        { catName: 'Găng tay' },
                        { catName: 'Phụ kiện tóc' },
                        { catName: 'Vòng tay & Lắc tay' },
                        { catName: 'Lắc chân' },
                        { catName: 'Mũ' },
                        { catName: 'Dây chuyền' },
                        { catName: 'Kính mắt' },
                        { catName: 'Kim loại quý' },
                        { catName: 'Thắt lưng' },
                        { catName: 'Cà vạt & Nơ cổ' },
                        { catName: 'Phụ kiện thêm' },
                        { catName: 'Bộ phụ kiện' },
                        { catName: 'Khác' },
                        { catName: 'Vớ/Tất' },
                        { catName: 'Ô/Dù' },
                    ]
                },
                {   name: 'BALO & TÚI VÍ NAM', 
                    cates: [
                        { catName: 'Ba Lô Nam' },
                        { catName: 'Ba Lô Laptop Nam' },
                        { catName: 'Túi & Cặp Đựng Laptop' },
                        { catName: 'Túi Chống Sốc Laptop Nam' },
                        { catName: 'Túi Tote Nam' },
                        { catName: 'Cặp Xách Công Sở Nam' },
                        { catName: 'Ví Cầm Tay Nam' },
                        { catName: 'Túi Đeo Hông & Túi Đeo Ngực Nam' },
                        { catName: 'Túi Đeo Chéo Nam' },
                        { catName: 'Bóp/Ví Nam' },
                        { catName: 'Khác' },
                    ]
                },
                {   name: 'VOUCHER & DỊCH VỤ', 
                    cates: [
                        { catName: 'Nhà hàng & Ăn uống' },
                        { catName: 'Sự kiện & Giải trí' },
                        { catName: 'Nạp tiền tài khoản' },
                        { catName: 'Sức khỏe & Làm đẹp' },
                        { catName: 'Gọi xe' },
                        { catName: 'Khóa học' },
                        { catName: 'Du lịch & Khách sạn' },
                        { catName: 'Mua sắm' },
                        { catName: 'Mã quà tặng Shopee' },
                        { catName: 'Thanh toán hóa đơn' },
                        { catName: 'Dịch vụ khác' },
                    ]
                },
                
            ]
        }
    }
}
</script>

<style scoped>
</style>