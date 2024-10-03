<template>
  <v-container>
    <v-row>
      <v-col cols="12" md="4">
        <v-list>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>Tài Khoản Của Tôi</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item v-for="(item, index) in menuItems" :key="index">
            <v-list-item-title>{{ item }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-col>

      <v-col col="12" md="8">
        <v-card>
          <v-card-title>Hồ sơ của tôi</v-card-title>
          <v-card-subtitle>Quản lý thông tin hồ sơ để bảo mật tài khoản</v-card-subtitle>
          <v-divider insert></v-divider>
          <v-card-text>
            <v-form>
              <v-row class="align-center">
                <v-col cols="4">
                  <p>Tên đăng nhập</p>
                </v-col>
                <v-col cols="4">
                  <v-text-field v-model="username" disabled hide-details></v-text-field>
                </v-col>
              </v-row>
            </v-form>
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
</style>