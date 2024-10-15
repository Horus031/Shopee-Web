<template>
  <v-container class="gird">
    <v-row>
      <v-col cols="12" sm="2">
        <ul>
          <li>Tài Khoản Của Tôi</li>
          <li v-for="(item, index) in menuItems" :key="index">{{ item }}</li>
        </ul>
      </v-col>
      <v-col cols="12" sm="10">
        <v-card class="pa-4">
          <v-card-title class="text-h5">Chỉnh sửa số điện thoại</v-card-title>
          <v-divider inset></v-divider>
          <v-card-text class="d-flex">
            <p>Số điện thoại mới</p>
            <div class="ml-16">
              <v-text-field v-model="phone" outlined dense hide-details></v-text-field>
              <v-btn class="my-5" color="orange darken-3" dark>Tiếp Theo</v-btn>
            </div>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      menuItems: [
        "Hồ Sơ",
        "Ngân Hàng",
        "Địa Chỉ",
        "Đổi Mật Khẩu",
        "Cài Đặt Thông Báo",
        "Những Thiết Lập Riêng Tư"
      ]
    };
  }
};
</script>

<style>
.grid {
  width: 1200px;
  max-width: 100%;
  margin: 0 auto;
}
li {
  list-style: none;
  margin: 10px;
}

::v-deep .v-application ul,
.v-application ol {
  padding: 0 !important;
}
</style>