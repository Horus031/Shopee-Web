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
                    <div class="caption" style="line-height: 1.4">
                        <span class="d-block" style="margin-left: 5px; margin-right: 12px">
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
    name: 'footerCategoriesCol5',
    data() {
        return {
            footerCategories: [
                {   name: 'Thiết Bị Điện Tử', 
                    cates: [
                        { catName: 'Thiết bị đeo thông minh' },
                        { catName: 'Phụ kiện tivi' },
                        { catName: 'Máy Game Console' },
                        { catName: 'Phụ kiện Console' },
                        { catName: 'Đĩa game' },
                        { catName: 'Linh phụ kiện' },
                        { catName: 'Tai nghe nhét tai' },
                        { catName: 'Loa' },
                        { catName: 'Tivi' },
                        { catName: 'Tivi Box' },
                        { catName: 'Headphones' },
                    ]
                },
                {   name: 'Sức Khỏe', 
                    cates: [
                        { catName: 'Vật tư y tế' },
                        { catName: 'Chống muỗi & xua đuổi côn trùng' },
                        { catName: 'Thực phẩm chức năng' },
                        { catName: 'Tã người lớn' },
                        { catName: 'Hỗ trợ làm đẹp' },
                        { catName: 'Hỗ trợ tình dục' },
                        { catName: 'Khác' },
                    ]
                },
                {   name: 'Thiết Bị Điện Gia Dụng', 
                    cates: [
                        { catName: 'Đồ gia dụng nhà bếp' },
                        { catName: 'Đồ gia dụng lớn' },
                        { catName: 'Máy hút bụi & Thiết bị làm sạch' },
                        { catName: 'Quạt & Máy nóng lạnh' },
                        { catName: 'Thiết bị chăm sóc quần áo' },
                        { catName: 'Khác' },
                        { catName: 'Máy xay, ép, máy đánh trứng trộn bột, máy xay thực phẩm' },
                        { catName: 'Bếp điện' },
                    ]
                },
                {   name: 'Nhà Sách Online', 
                    cates: [
                        { catName: 'Sách Tiếng Việt' },
                        { catName: 'Sách ngoại văn' },
                        { catName: 'Gói Quà' },
                        { catName: 'Bút viết' },
                        { catName: 'Dụng cụ học sinh & văn phòng' },
                        { catName: 'Màu, Họa Cụ và Đồ Thủ Công' },
                        { catName: 'Sổ và Giấy Các Loại' },
                        { catName: 'Quà Lưu Niệm' },
                        { catName: 'Nhạc cụ và phụ kiện âm nhạc' },
                    ]
                },
                {   name: 'Chăm Sóc Thú Cưng', 
                    cates: [
                        { catName: 'Thức ăn cho thú cưng' },
                        { catName: 'Phụ kiện cho thú cưng' },
                        { catName: 'Vệ sinh cho thú cưng' },
                        { catName: 'Quần áo thú cưng' },
                        { catName: 'Chăm sóc sức khỏe' },
                        { catName: 'Làm đẹp cho thú cưng' },
                        { catName: 'Khác' },
                    ]
                },
            ]
        }
    }
}
</script>

<style scoped>

</style>