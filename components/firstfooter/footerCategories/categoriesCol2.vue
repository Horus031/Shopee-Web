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
    name: 'footerCategoriesCol2',
    data() {
        return {
            footerCategories: [
                {   name: 'Thời Trang Nữ', 
                    cates: [
                        { catName: 'Quần' },
                        { catName: 'Quần đùi' },
                        { catName: 'Chân váy' },
                        { catName: 'Quần Jeans' },
                        { catName: 'Đầm/Váy' },
                        { catName: 'Váy cưới' },
                        { catName: 'Đồ liền thân' },
                        { catName: 'Áo khoác, Áo choàng & Vest' },
                        { catName: 'Áo len & Cardigan' },
                        { catName: 'Hoodie và Áo nỉ' },
                        { catName: 'Bộ' },
                        { catName: 'Đồ lót' },
                        { catName: 'Đồ ngủ' },
                        { catName: 'Áo' },
                        { catName: 'Đồ tập' },
                        { catName: 'Đồ bầu' },
                        { catName: 'Đồ truyền thống' },
                        { catName: 'Đồ hóa trang' },
                        { catName: 'Vải' },
                        { catName: 'Vớ/Tất' },
                        { catName: 'Khác' },
                        
                    ]
                },
                {   name: 'Máy Tính & Laptop', 
                    cates: [
                        { catName: 'Máy Tính Bàn' },
                        { catName: 'Màn Hình' },
                        { catName: 'Linh Kiện Máy Tính' },
                        { catName: 'Thiết Bị Lưu Trữ' },
                        { catName: 'Thiết Bị Mạng' },
                        { catName: 'Máy In, Máy Scan & Máy Chiếu' },
                        { catName: 'Phụ Kiện Máy Tính' },
                        { catName: 'Laptop' },
                        { catName: 'Khác' },
                        { catName: 'Gaming' },
                    ]
                },
                {   name: 'Giày Dép Nữ', 
                    cates: [
                        { catName: 'Bốt' },
                        { catName: 'Giày Thể Thao/ Sneaker' },
                        { catName: 'Giày Đế Bằng' },
                        { catName: 'Giày Cao Gót' },
                        { catName: 'Giày Đế Xuồng' },
                        { catName: 'Xăng-đan Và Dép' },
                        { catName: 'Phụ Kiện Giày' },
                        { catName: 'Giày Khác' },
                    ]
                },
                {   name: 'Thể Thao & Du Lịch', 
                    cates: [
                        { catName: 'Vali' },
                        { catName: 'Túi du lịch' },
                        { catName: 'Phụ kiện du lịch' },
                        { catName: 'Dụng Cụ Thể Thao & Dã Ngoại' },
                        { catName: 'Giày Thể Thao' },
                        { catName: 'Thời Trang Thể Thao & Dã Ngoại' },
                        { catName: 'Phụ Kiện Thể Thao & Dã Ngoại' },
                        { catName: 'Khác' },
                    ]
                },
                {   name: 'Thời Trang Trẻ Em', 
                    cates: [
                        { catName: 'Trang phục bé trai' },
                        { catName: 'Trang phục bé gái' },
                        { catName: 'Giày dép bé trai' },
                        { catName: 'Giày dép bé gái' },
                        { catName: 'Khác' },
                        { catName: 'Quần áo em bé' },
                        { catName: 'Giày tập đi & Tất sơ sinh' },
                        { catName: 'Phụ kiện trẻ em' },
                    ]
                },
                {   name: 'Dụng cụ và thiết bị tiện ích', 
                    cates: [
                        { catName: 'Dụng cụ cầm tay' },
                        { catName: 'Dụng cụ điện và thiết bị lớn' },
                        { catName: 'Thiết bị mạch điện' },
                        { catName: 'Vật liệu xây dựng' },
                        { catName: 'Thiết bị và phụ kiện xây dựng' },
                    ]
                },
                
            ]
        }
    }
}
</script>

<style scoped>

</style>