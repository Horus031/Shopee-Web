<template>
    <v-sheet color="grey lighten-4 pt-5" >
        <v-card class="grid" flat tile style="border-bottom: 1px solid #f5f5f5;">
            <v-card-title>
                <h5 class="font-weight-light">DANH MỤC</h5>
            </v-card-title>
        </v-card>
        <v-card class="grid overflow-x-auto" rounded="sm" tile flat>
            <v-sheet color="transparent d-flex flex-wrap" max-height="312px" width="142%"> 
                <v-card tile class="d-flex flex-wrap align-center" color="transparent">
                    <v-hover v-for="(category, index) in categories" :key="index" v-slot="{ hover }" >
                        <v-card :elevation="hover ? 2 : 0" class="d-flex flex-column align-center" max-width="119px" height="150px" style="padding: 18px;">
                            <a href="" class="text-decoration-none black--text text-center d-flex flex-column align-center" style="text-wrap: wrap; width: 100px">
                                <v-img
                                    :src="category.src"
                                    max-width="83px"
                                    max-height="83px"
                                    contain
                                >

                                </v-img>
                            
                                <span class="text-center caption"> {{ category.name }}</span>
                            </a>
                        </v-card>
                    </v-hover>
                </v-card>
            </v-sheet>
        </v-card>
    </v-sheet>
</template>

<script>
export default {
    name: 'bodyProductCategory',
    data() {
        return {
            categories: [
                { name: 'Thời Trang Nam', src: "https://down-vn.img.susercontent.com/file/687f3967b7c2fe6a134a2c11894eea4b" },
                { name: 'Điện Thoại & Phụ Kiện', src: "https://down-vn.img.susercontent.com/file/31234a27876fb89cd522d7e3db1ba5ca" },
                { name: 'Thiết Bị Điện Tử', src: "https://down-vn.img.susercontent.com/file/978b9e4cb61c611aaaf58664fae133c5" },
                { name: 'Máy Tính & Laptop', src: "https://down-vn.img.susercontent.com/file/c3f3edfaa9f6dafc4825b77d8449999d" },
                { name: 'Máy Ảnh & Máy Quay Phim', src: "https://down-vn.img.susercontent.com/file/ec14dd4fc238e676e43be2a911414d4d" },
                { name: 'Đồng Hồ', src: "https://down-vn.img.susercontent.com/file/86c294aae72ca1db5f541790f7796260" },
                { name: 'Giày Dép Nam', src: "https://down-vn.img.susercontent.com/file/74ca517e1fa74dc4d974e5d03c3139de" },
                { name: 'Thiết Bị Điện Gia Dụng', src: "https://down-vn.img.susercontent.com/file/7abfbfee3c4844652b4a8245e473d857" },
                { name: 'Thể Thao & Du Lịch', src: "https://down-vn.img.susercontent.com/file/6cb7e633f8b63757463b676bd19a50e4" },
                { name: 'Ô Tô & Xe Máy & Xe Đạp', src: "https://down-vn.img.susercontent.com/file/3fb459e3449905545701b418e8220334" },
                { name: 'Balo & Túi Ví Nam', src: "https://down-vn.img.susercontent.com/file/18fd9d878ad946db2f1bf4e33760c86f" },
                { name: 'Đồ Chơi', src: "https://down-vn.img.susercontent.com/file/ce8f8abc726cafff671d0e5311caa684" },
                { name: 'Chăm Sóc Thú Cưng', src: "https://down-vn.img.susercontent.com/file/cdf21b1bf4bfff257efe29054ecea1ec" },
                { name: 'Dụng cụ và thiết bị tiện ích', src: "https://down-vn.img.susercontent.com/file/e4fbccba5e1189d1141b9d6188af79c0" },
                { name: 'Thời Trang Nữ', src: "https://down-vn.img.susercontent.com/file/75ea42f9eca124e9cb3cde744c060e4d" },
                { name: 'Mẹ & Bé', src: "https://down-vn.img.susercontent.com/file/099edde1ab31df35bc255912bab54a5e" },
                { name: 'Nhà Cửa & Đời Sống', src: "https://down-vn.img.susercontent.com/file/24b194a695ea59d384768b7b471d563f" },
                { name: 'Sắc Đẹp', src: "https://down-vn.img.susercontent.com/file/ef1f336ecc6f97b790d5aae9916dcb72" },
                { name: 'Sức Khỏe', src: "https://down-vn.img.susercontent.com/file/49119e891a44fa135f5f6f5fd4cfc747" },
                { name: 'Giày Dép Nữ', src: "https://down-vn.img.susercontent.com/file/48630b7c76a7b62bc070c9e227097847" },
                { name: 'Túi Ví Nữ', src: "https://down-vn.img.susercontent.com/file/fa6ada2555e8e51f369718bbc92ccc52" },
                { name: 'Phụ Kiện & Trang Sức Nữ', src: "https://down-vn.img.susercontent.com/file/8e71245b9659ea72c1b4e737be5cf42e" },
                { name: 'Bách Hóa Online', src: "https://down-vn.img.susercontent.com/file/c432168ee788f903f1ea024487f2c889" },
                { name: 'Nhà Sách Online', src: "https://down-vn.img.susercontent.com/file/36013311815c55d303b0e6c62d6a8139" },
                { name: 'Thời Trang Trẻ Em', src: "https://down-vn.img.susercontent.com/file/4540f87aa3cbe99db739f9e8dd2cdaf0" },
                { name: 'Giặt Giũ & Chăm Sóc Nhà Cửa', src: "https://down-vn.img.susercontent.com/file/cd8e0d2e6c14c4904058ae20821d0763" },
                { name: 'Voucher & Dịch Vụ', src: "https://down-vn.img.susercontent.com/file/b0f78c3136d2d78d49af71dd1c3f38c1" },
            ],
        }
    }
}
</script>

<style scoped>
.grid {
    width: 1200px;
    max-width: 100%;
    margin: 0 auto;
}
</style>