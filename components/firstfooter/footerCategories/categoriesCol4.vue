<template>
    <div>
        <div>
            <div v-for="(footerCate, index) in footerCategories" :key="index"> 
                <div>
                    <div style="margin: 7px 0px 0px 5px; padding: 2px 0">
                        <v-hover v-slot="{ hover }">
                            <a
                                :class="hover ? 'shopeecolor--text' : 'grey--text darken-4'"
                                href="" 
                                class="caption text-decoration-none font-weight-bold text-uppercase"
                            >
                                {{ footerCate.name }}
                            </a>
                        </v-hover>
                    </div>
                </div>

                <div class="d-flex flex-wrap mb-2" style="margin-top: -2px;">
                    <div class="caption" style="line-height: 1.4;">
                        <span class="d-block" style="margin-left: 5px; margin-right: 12px;">
                            <span 
                                v-for="(cate, index) in footerCate.cates" 
                                :key="index" 
                                class="grey--text lighten-2 font-weight-light text-capitalize"
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
    name: 'footerCategoriesCol4',
    data() {
        return {
            footerCategories: [
                {   name: 'Mẹ & Bé', 
                    cates: [
                        { catName: 'Đồ dùng du lịch cho bé' },
                        { catName: 'Đồ dùng ăn dặm cho bé' },
                        { catName: 'Phụ kiện cho mẹ' },
                        { catName: 'Chăm sóc sức khỏe mẹ' },
                        { catName: 'Quần Dài/Quần Âu' },
                        { catName: 'Đồ dùng phòng tắm & Chăm sóc cơ thể bé' },
                        { catName: 'Đồ dùng phòng ngủ cho bé' },
                        { catName: 'An toàn cho bé' },
                        { catName: 'Thực phẩm cho bé' },
                        { catName: 'Chăm sóc sức khỏe bé' },
                        { catName: 'Tã & bô em bé' },
                        { catName: 'Đồ chơi' },
                        { catName: 'Bộ & Gói quà tặng' },
                        { catName: 'Khác' },
                        { catName: 'Sữa công thức trên 24 tháng' },
                        { catName: 'Sữa công thức 0-24 tháng tuổi' },
                    ]
                },
                {   name: 'Máy Ảnh & Máy Quay Phim', 
                    cates: [
                        { catName: 'Máy ảnh - Máy quay phim' },
                        { catName: 'Camera giám sát & Camera hệ thống' },
                        { catName: 'Thẻ nhớ' },
                        { catName: 'Ống kính' },
                        { catName: 'Phụ kiện máy ảnh' },
                        { catName: 'Máy bay camera & Phụ kiện' },
                    ]
                },
                {   name: 'Túi Ví Nữ', 
                    cates: [
                        { catName: 'Ba Lô Nữ' },
                        { catName: 'Cặp Laptop' },
                        { catName: 'Ví Dự Tiệc & Ví Cầm Tay' },
                        { catName: 'Túi Đeo Hông & Túi Đeo Ngực' },
                        { catName: 'Túi Tote' },
                        { catName: 'Túi Quai Xách' },
                        { catName: 'Túi Đeo Chéo & Túi Đeo Vai' },
                        { catName: 'Ví/Bóp Nữ' },
                        { catName: 'Phụ Kiện Túi' },
                        { catName: 'Khác' },
                    ]
                },
                {   name: 'Ô Tô & Xe Máy & Xe Đạp', 
                    cates: [
                        { catName: 'Xe đạp, xe điện' },
                        { catName: 'Mô tô, xe máy' },
                        { catName: 'Xe Ô tô' },
                        { catName: 'Mũ bảo hiểm' },
                        { catName: 'Phụ kiện xe máy' },
                        { catName: 'Phụ kiện xe đạp' },
                        { catName: 'Phụ kiện bên trong ô tô' },
                        { catName: 'Dầu nhớt & dầu nhờn' },
                        { catName: 'Phụ tùng ô tô' },
                        { catName: 'Phụ tùng xe máy' },
                        { catName: 'Phụ kiện bên ngoài ô tô' },
                        { catName: 'Chăm sóc ô tô' },
                        { catName: 'Dịch vụ cho xe' },
                    ]
                },
                {   name: 'Giặt Giũ & Chăm Sóc Nhà Cửa', 
                    cates: [
                        { catName: 'Giặt giũ & Chăm sóc nhà cửa' },
                        { catName: 'Giấy vệ sinh, khăn giấy' },
                        { catName: 'Vệ sinh nhà cửa' },
                        { catName: 'Vệ sinh bát đĩa' },
                        { catName: 'Dụng cụ vệ sinh' },
                        { catName: 'Chất khử mùi, làm thơm' },
                        { catName: 'Thuốc diệt côn trùng' },
                        { catName: 'Túi, màng bọc thực phẩm' },
                        { catName: 'Bao bì, túi đựng rác' },
                    ]
                },
            ]
        }
    }
}
</script>

<style scoped>

</style>