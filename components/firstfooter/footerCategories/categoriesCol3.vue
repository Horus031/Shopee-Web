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
    name: 'footerCategoriesCol3',
    data() {
        return {
            footerCategories: [
                {   name: 'Điện Thoại & Phụ Kiện', 
                    cates: [
                        { catName: 'Điện thoại' },
                        { catName: 'Máy tính bảng' },
                        { catName: 'Pin Dự Phòng' },
                        { catName: 'Pin Gắn Trong, Cáp và Bộ Sạc' },
                        { catName: 'Ốp lưng, bao da, Miếng dán điện thoại' },
                        { catName: 'Bảo vệ màn hình' },
                        { catName: 'Đế giữ điện thoại' },
                        { catName: 'Thẻ nhớ' },
                        { catName: 'Sim' },
                        { catName: 'Phụ kiện khác' },
                        { catName: 'Thiết bị khác' },
                    ]
                },
                {   name: 'Sắc Đẹp', 
                    cates: [
                        { catName: 'Chăm sóc da mặt' },
                        { catName: 'Tắm & chăm sóc cơ thể' },
                        { catName: 'Trang điểm' },
                        { catName: 'Chăm sóc tóc' },
                        { catName: 'Dụng cụ & Phụ kiện Làm đẹp' },
                        { catName: 'Vệ sinh răng miệng' },
                        { catName: 'Nước hoa' },
                        { catName: 'Chăm sóc nam giới' },
                        { catName: 'Khác' },
                        { catName: 'Chăm sóc phụ nữ' },
                        { catName: 'Bộ sản phẩm làm đẹp' },
                    ]
                },
                {   name: 'Giày Dép Nam', 
                    cates: [
                        { catName: 'Bốt' },
                        { catName: 'Giày Thể Thao/ Sneakers' },
                        { catName: 'Giày Sục' },
                        { catName: 'Giày Tây Lười' },
                        { catName: 'Giày Oxfords & Giày Buộc Dây' },
                        { catName: 'Xăng-đan và Dép' },
                        { catName: 'Phụ kiện giày dép' },
                        { catName: 'Khác' },
                    ]
                },
                {   name: 'Bách Hóa Online', 
                    cates: [
                        { catName: 'Đồ ăn vặt' },
                        { catName: 'Đồ chế biến sẵn' },
                        { catName: 'Nhu yếu phẩm' },
                        { catName: 'Nguyên liệu nấu ăn' },
                        { catName: 'Đồ làm bánh' },
                        { catName: 'Sữa - trứng' },
                        { catName: 'Đồ uống' },
                        { catName: 'Ngũ cốc & mứt' },
                        { catName: 'Các loại bánh' },
                        { catName: 'Đồ uống có cồn' },
                        { catName: 'Bộ quà tặng' },
                        { catName: 'Thực phẩm tươi sống và thực phẩm đông lạnh' },
                        { catName: 'Khác' },
                    ]
                },
                {   name: 'Đồ Chơi', 
                    cates: [
                        { catName: 'Sở thích & Sưu tầm' },
                        { catName: 'Đồ chơi giải trí' },
                        { catName: 'Đồ chơi giáo dục' },
                        { catName: 'Đồ chơi cho trẻ sơ sinh & trẻ nhỏ' },
                        { catName: 'Đồ chơi vận động & ngoài trời' },
                        { catName: 'Búp bê & Đồ chơi nhồi bông' },
                    ]
                },
            ]
        }
    }
}
</script>

<style scoped>

</style>